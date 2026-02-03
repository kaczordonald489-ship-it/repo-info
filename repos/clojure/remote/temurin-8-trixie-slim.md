## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:96a326a707f2135a94910b0beb7d03926f1c5d241e4337fc1fecedf68dbde3ad
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
$ docker pull clojure@sha256:f4ae50dbc9994f9715bc240aff3a41dbe2e027e53c826ff6f2fc41b3d2bd8ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156508451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1a364750b0dc4f8c371054b9e62667ce2e2ea8c408d35b2adc5fce6fdecb2b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:17:59 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:18:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:18:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5d23877b51c01d1e3dd5916935066d4accc854310db45c2a02af8943165e64`  
		Last Modified: Tue, 03 Feb 2026 03:18:32 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e24148846e3db49b7f099f2406326718007cdfde810b4adc9583818d94bef1b`  
		Last Modified: Tue, 03 Feb 2026 03:19:13 GMT  
		Size: 72.0 MB (71995838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25185a308338ebfb5a768f87740ac1230bc9e2d09b254947c0be23f61640c5e8`  
		Last Modified: Tue, 03 Feb 2026 03:19:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7065db29878a2a1161c28da21476f430c0aba7c991b458e5737756979e688dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c7da56abdf61f8a7e1f6496675d41f1354c328671331d3f7c850fd2ca415f9`

```dockerfile
```

-	Layers:
	-	`sha256:f896e669c0eb9ff70cf2570efd3c92f6bea71499225a6336eb69b1489ce2760f`  
		Last Modified: Tue, 03 Feb 2026 03:19:11 GMT  
		Size: 5.4 MB (5377907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdfc8487379f417dd1c68b840e044eab8a8b8a7785de367b688de1444e125a8`  
		Last Modified: Tue, 03 Feb 2026 03:19:11 GMT  
		Size: 13.4 KB (13428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b53c800d6dca67944632ba66d56c36573d9152d589fc650c541779339cf78a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155762304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6dbd08d1a0fe1e1acfd341b6c6b99932add24dbc52c859e4754abaad293bea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:36 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2047505dae0c83b30a65b712ee6c0a65147c64e896e0370d771362f22c96fb7`  
		Last Modified: Tue, 03 Feb 2026 03:21:08 GMT  
		Size: 53.8 MB (53814976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dac25450c753f915e11e654fc7928b19321b6da277fba928934ca8207123f5c`  
		Last Modified: Tue, 03 Feb 2026 03:21:49 GMT  
		Size: 71.8 MB (71806616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00001c6515ea0fa308423a553db9e70471c8094dbd5c3630a39bf51b98266846`  
		Last Modified: Tue, 03 Feb 2026 03:21:47 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d113a8d21b96429055a1883d8acddc52aa5f888bc59ef78fa3a4c7d79815b660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb241c03f1f7cf36f3ab01c7944464681c66eb01372be45622ebe23d80a092b`

```dockerfile
```

-	Layers:
	-	`sha256:739838a255bc6e802c47a4d73dcba720050557bc084fb6a36bb6c1dec7f5a6de`  
		Last Modified: Tue, 03 Feb 2026 03:21:48 GMT  
		Size: 5.4 MB (5384374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f3c15520ea0578c1b070c3297f07e3d41b515770cd1327979e35264b6e8b00`  
		Last Modified: Tue, 03 Feb 2026 03:21:47 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:951f2e20f8279bb77467315c99a1946e66cd872f6a69fe7bacf8d783003d755f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166362448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6969f07ef105179e5ffb470cd407edb1a0a9126e76c1c8659b3e56bde480bc15`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:16:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:16:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:16:03 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:17:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:17:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:17:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faf783503dc7dd62a80622a59f1d7d097ae81140a522e1cc754dfca95c0390b`  
		Last Modified: Wed, 28 Jan 2026 18:17:43 GMT  
		Size: 52.2 MB (52175145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5370dbc603da3d91b0ddc9fcf48a0224b53f74588a50b4a05ea59a54f3e67f8c`  
		Last Modified: Wed, 28 Jan 2026 18:17:43 GMT  
		Size: 80.6 MB (80591059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc44f6629641099f7063fe4f627855e0b0922841a4c31fc5c91bef452c5524a1`  
		Last Modified: Wed, 28 Jan 2026 18:17:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5e3a9a270d22258f7ad8f0066f9a05bc41a849fe777e7e38ad1117b1fe027c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a324984fbdac1f7b76427beb6321a459a065d490624ddf9a010688d8194c0a7`

```dockerfile
```

-	Layers:
	-	`sha256:2bb3ce332b514a02cf1190781c8a302945d6f9e20ce373a9b2926e8bafe238c6`  
		Last Modified: Wed, 28 Jan 2026 18:17:41 GMT  
		Size: 5.4 MB (5382871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a51549d9b369970457f3bd4a1f751a7b9db108324265c836fae29e4f768d95`  
		Last Modified: Wed, 28 Jan 2026 18:17:40 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
