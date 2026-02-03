## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:7a36525510041343f0a59437ab8945af8eb2ffa0cabfdeee905b3e0247e2b14d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ffe11de0e9c6eaa892c736dc0a231cb83770d66979e435331b9d4f0085b0a187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247221955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab35cb5f28e48f7df673638139d81f2e8ed802c256961fac528966e21294c7b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c2aa59f787ba75f1eeede3ecf72db034ac20ba840738d7e2ff182ec9162284`  
		Last Modified: Tue, 03 Feb 2026 03:22:34 GMT  
		Size: 157.8 MB (157826002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcfb7749fe405f45176d2b69f43c19c7dc021f49ca20865036e3cabcf48a963`  
		Last Modified: Tue, 03 Feb 2026 03:22:32 GMT  
		Size: 59.1 MB (59136625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5f04cf0193fba7a34c7e5c432a53ccba5f461f9878315b04e99760f069e055`  
		Last Modified: Tue, 03 Feb 2026 03:22:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd502e39545f372587fb96322ada29876fb185e7d4cfd67609b7fda1e185ae24`  
		Last Modified: Tue, 03 Feb 2026 03:22:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f217cca8711603574fdb500a2cb9980effab0564698105f0e40a308c4410ed79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d67c1e453f84558ce846cb21f50de48dff7f4362a847c5b4e3f223a89012bd`

```dockerfile
```

-	Layers:
	-	`sha256:2172f7347faa183d1eb7ce788d54d8b194fff655a192150f4c7d58263fd2ab31`  
		Last Modified: Tue, 03 Feb 2026 03:22:30 GMT  
		Size: 5.3 MB (5311970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8532a4e434ea27e277e8f995451c10a262e5f16d7222b66d3380ec02668d02d`  
		Last Modified: Tue, 03 Feb 2026 03:22:30 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e41aa1c28e852b6b61d0c0eae612f29db4845232fa4f662ba6cd0fbd664a854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244141057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbf69e659a496a76abe754f5e9ca2dd712676a40ec0ec337c454faa96547f17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:49:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:49:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:49:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:49:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:26 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067bb3bbe074612276c9f939e8d48692e24f69f52f44cd55f565c383c1fd03b6`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b916916de254bb6c115a7e8008bb2320b07adef07e476ef7d05003528b91d83`  
		Last Modified: Tue, 03 Feb 2026 03:24:55 GMT  
		Size: 59.3 MB (59287925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b684694d014393a70de6e247a96b3594a7d0b6876f917cce1f5be97bb6359d5`  
		Last Modified: Tue, 03 Feb 2026 03:24:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a936cab650dfdcf10e88eb96d7ef8395be22e18fc131c27b059efd05643b194`  
		Last Modified: Tue, 03 Feb 2026 03:24:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ffb88cd3e1c6f609456f0f057840501f7b0526153918059ed276c7ce0b3bafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1255b3ae58a5fcdbddd05fa9a349214fc4354eedff2bec6f77798d4789e0dc87`

```dockerfile
```

-	Layers:
	-	`sha256:0aaae5ed98e3e317eb1e10d80a6eb26d4b6f327d435fefc872a3b681e39a6c28`  
		Last Modified: Tue, 03 Feb 2026 03:24:53 GMT  
		Size: 5.3 MB (5317702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07e10bb36c6b4f087724b63d50c494f5afa727e62858172fb4ada379e89f740e`  
		Last Modified: Tue, 03 Feb 2026 03:24:53 GMT  
		Size: 15.2 KB (15153 bytes)  
		MIME: application/vnd.in-toto+json
