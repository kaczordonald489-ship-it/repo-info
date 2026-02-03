## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:b91def0de93c4d643bacfc27616c8ac5903518397ec31c62f0ab43e4cd33f7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0709c21dd05d9aec395c85166188c62631e12e3df8f5f79bf7284ab38b866b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234244206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac28b9f8f73d03bb3cd867c4a5103eecdce3fab36dc60531951f03b74a4dbf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:21:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:21:04 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f09812529f4da6bd3f47da903988d2829ab2a4e604d32482686bd4ddf78395f`  
		Last Modified: Tue, 03 Feb 2026 03:21:37 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8784268f0ffe67bd7103938e4fdf60d2627da73c19a5b0c1db12309d6f7cf9d`  
		Last Modified: Tue, 03 Feb 2026 03:21:36 GMT  
		Size: 59.1 MB (59136934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3108da3ca0e0d2ad76ce3ce17798b316b6f7c26cae4de77a5f1c771e70856613`  
		Last Modified: Tue, 03 Feb 2026 03:21:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b8accdd4a2d0a419f427dd836337b333a1593a747249847a940fdeb95d208a`  
		Last Modified: Tue, 03 Feb 2026 03:21:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba02e6dcf1c458bf65f2146fb282d3a67e1fc6c1b4618f514fb2861286ae743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5324704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e889420989ddea1bf8b058af198d8fe5853b874ff06c3313f1188c31d7855c1`

```dockerfile
```

-	Layers:
	-	`sha256:319dbd325052664f52525b19bb77a093c191937b87eb8ba8b5be82132dcafcd0`  
		Last Modified: Tue, 03 Feb 2026 03:21:33 GMT  
		Size: 5.3 MB (5308868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1239f264e711e7a1db9665bd23498fb2da73fc8707d2c45f086a836583cc531d`  
		Last Modified: Tue, 03 Feb 2026 03:21:33 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61ddfc2bb98e733ffa1b20583b8cfd32e3e1c6cac4a2faeb5885d1391c1fa035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231713401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f266a44e5dec1e85720d73660c8ae803eca8609a6a61f2ba581cd0bf15f7b8e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:50:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:50:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:50:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:26 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:15 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad13db4a3cb775f09081840bd13b0c321e9d57f716ff9d24395b6d5b73cbf01`  
		Last Modified: Tue, 03 Feb 2026 02:51:26 GMT  
		Size: 143.7 MB (143679941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137fe37f2e751e8658d6823ee66cbc8fe74adad78b829882dae7f2ba739c3f86`  
		Last Modified: Tue, 03 Feb 2026 03:23:43 GMT  
		Size: 59.3 MB (59287980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb9397a3690148f487ff1b5c262d9b00d8ffcd35992d97f4069d6c26abb2ac6`  
		Last Modified: Tue, 03 Feb 2026 03:23:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796c5b111827b49b883a86c741e2a0e804e0d94c2d6348dd04273a02fe9f2f63`  
		Last Modified: Tue, 03 Feb 2026 03:23:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:334c29a370a4907c0c7f362c0773ebc31759ea6fb7a736a4d1026337aa4316ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ef216aa0283c08a510daf5ce4de706c148d4461f9e9f51528be9fd3d3833f2`

```dockerfile
```

-	Layers:
	-	`sha256:a06c8b0b7e3833906025d0da0a048b397e3a41a8b442cbe7d952bee3f1c4f2f0`  
		Last Modified: Tue, 03 Feb 2026 03:23:41 GMT  
		Size: 5.3 MB (5314600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb9dcf0afadcd821b978c820341aec3f3a2d687174950d8a9d10f26d3289c49`  
		Last Modified: Tue, 03 Feb 2026 03:23:41 GMT  
		Size: 15.2 KB (15152 bytes)  
		MIME: application/vnd.in-toto+json
