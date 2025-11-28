## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:1a948cafbb22a291159167ff52a6c92d368f9657790e57f333b9719a34759af9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a18fda51fe1b2990719f9983f40fa01b0c90bae06fa9e8adce7ed529c913de16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181456722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c59e1606d54b90908dd0ce6707b44f96437a990f6ae7bba407c4e1e7ca8abd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:17:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:17:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:17:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:17:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:17:55 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:18:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:18:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:18:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:18:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:18:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241dafc70a30d70567c4489a8137e12d10ae631fa59b3d773fa4e0d3f2b6622e`  
		Last Modified: Tue, 18 Nov 2025 06:18:53 GMT  
		Size: 92.0 MB (92045322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac61b72331ff0ee24075d229611a87edc737d4f4d3d39ede31aa3fabe0b005b`  
		Last Modified: Tue, 18 Nov 2025 06:18:50 GMT  
		Size: 59.2 MB (59151877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15afcb07cd592e45cabb625c6f15bca7c5d6f8d78d8f5746b10b9434fea5b7d8`  
		Last Modified: Tue, 18 Nov 2025 06:18:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de7ec8569a2572ff6f789ec0984fc30b260c3df5818eed6e777068ffda2d6b2`  
		Last Modified: Tue, 18 Nov 2025 06:18:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7292360dc42d10dae5ca50a5acecfee32eacff59172bd481b431fac1954b6f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed9a7677492ff8a69183d8dcb65386c6992dbf68fbde59ea410d6fc7f414697`

```dockerfile
```

-	Layers:
	-	`sha256:63ac544df71c9325cb1131e60e1aa08c3f77b5c547f477edc01cbbc16c642ceb`  
		Last Modified: Tue, 18 Nov 2025 07:47:31 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37bf7eea9490fc2d537a5b08e50ab350d0ef9a97c595d9fec43a993a9378993d`  
		Last Modified: Tue, 18 Nov 2025 07:47:32 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:558c621688758f834de3557dfcd2daf4120b71187e0d97c15b2b2dcd13dbff77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179089557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cf16419c93c0e25f286df088fb069ea4a32aab903fd5eba2e969e4b0c925d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:13:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:13:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:13:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:13:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:13:19 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:16:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:16:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:16:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:16:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:16:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb35b5a53c49e819271cc9161dc95a3ee8a2bce03037253eeaefa3a7062c192d`  
		Last Modified: Tue, 18 Nov 2025 05:14:17 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0e4d3a31b6e9a9ae419cf38627320f084ff022a794b70e8d20d1a8bd92a0bd`  
		Last Modified: Tue, 18 Nov 2025 05:16:47 GMT  
		Size: 59.3 MB (59287537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170fa4b0ce8532a53101454fb7b31587bb18529e3192463a2d6b266008bbe4cc`  
		Last Modified: Tue, 18 Nov 2025 05:16:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751baeb9a20a8e7510a4fafcdce5a8a6bc7861d3c4d5b7ffa56d6bcca79f8c6f`  
		Last Modified: Tue, 18 Nov 2025 05:16:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e0795935a0656a635bb6f17607fa4c003a7682f1c4f3e266fe904a3d20e2802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620a0fdf8db07574f5ec081c5d4c77e0196bb42d05beaee2bc81def890cf01ab`

```dockerfile
```

-	Layers:
	-	`sha256:5426aaaa3cace6b7f6aa2bf4e56979cec71ab3c1c3e060f0e49ae7aedaaec0af`  
		Last Modified: Tue, 18 Nov 2025 07:47:38 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7eb57e619945955f6341190acd2f0f8a26974f3a6a48fcaa8668218a2b6f86`  
		Last Modified: Tue, 18 Nov 2025 07:47:38 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json
