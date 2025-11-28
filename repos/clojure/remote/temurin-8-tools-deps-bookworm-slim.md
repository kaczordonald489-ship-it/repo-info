## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:99113e321743c07f864caeab25b91b4a491496ab7617ef885bee2400a84f3128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f9c85ff4985a86e406031b9705a5ed41ceef3b337ccf22a897378efd4f9cb263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152641302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9e7a06b59900feb95f40e57ab73966dd9b04bf3265359d06b8ddf04d4ce90a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:05:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:49 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:05:49 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:06:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:06:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:06:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ec5c403d5399c416e46514b67a7fa7cab1b1b575ff56520eb702dca6c3059e`  
		Last Modified: Tue, 18 Nov 2025 06:06:36 GMT  
		Size: 54.7 MB (54733390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3576e1c01ee2ac5d5b1ff0087ecef3a42c95242eedda15e40fca46cb23abb9`  
		Last Modified: Tue, 18 Nov 2025 06:06:46 GMT  
		Size: 69.7 MB (69678818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80adc96800a19c11256d251a655917c611e6ce2bcdd52d32aaf092050c89915f`  
		Last Modified: Tue, 18 Nov 2025 06:06:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bdb5bbfe10985594d7eced6dec6e72e7e03d64575a5eb99bf3ef1dd6920d79cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c65caf98bc89c83942696c8613b9e2ac36f1c36c64b28a7dd6fcbb5af3095a`

```dockerfile
```

-	Layers:
	-	`sha256:256e277415e5e7c5af343aed1b05f9c0ffb564e8eb0f3ea2313f7f36c3fc9ccd`  
		Last Modified: Tue, 18 Nov 2025 07:49:27 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78c8a05385a0f62691acc0a7edda9386e24f0d44713493bd593452eeaea9786`  
		Last Modified: Tue, 18 Nov 2025 07:49:28 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f8243ceb5d519691e26afc74c250af3b6524e6d453d73c3c2dea98c9ad4f08f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151478272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d04f0ed9b666333bae3c36d0b2f449b908ae60ad35df38bcd2710131c4d038`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:53:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:53:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:53:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:53:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:53:28 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:53:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:53:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:53:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5174cc92a98c3126b6fa025f8a8e5dbc830073993e045d75383dfa17d30ba1b`  
		Last Modified: Tue, 18 Nov 2025 04:54:15 GMT  
		Size: 53.8 MB (53814999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6193d376ef0fc7831f4ab1d2e22e65e74390b1ada725a94177a4223a190ae1d0`  
		Last Modified: Tue, 18 Nov 2025 04:54:12 GMT  
		Size: 69.6 MB (69560422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436502cde57999701d107ba53c1639c783c500c0416bffa05d5904f040eb8c7f`  
		Last Modified: Tue, 18 Nov 2025 04:54:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f67aec0c89fb339ff5d92ec6a82cff56c9e5aa8822358842994a6c4eed3b3a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510e872e056d941bc85849f41609f096a34000bb0771a4990c7ffb24b1fc7406`

```dockerfile
```

-	Layers:
	-	`sha256:f561a284d879aeb66f4e7dc2216c77e9417ef07a35ffafd14080011d066191f5`  
		Last Modified: Tue, 18 Nov 2025 07:49:33 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e244b0d35976c363a7bcb2670e6908389725d3bcd52a762161529f6eebdcf0`  
		Last Modified: Tue, 18 Nov 2025 07:49:34 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4b1e3e94998a362b475352c55cead401549648209ec90103956f5021dee86a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159757875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b7c4b98597450bf32f2da7072d966ff19c0c80e0797ba50d713b8029214495`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:14:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:14:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:14:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:14:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:14:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:17:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:17:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:17:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d016d9e912cb735827e82c51514523b6941a4ca5114f7db6b8ad862763e4a5`  
		Last Modified: Tue, 18 Nov 2025 06:15:45 GMT  
		Size: 52.2 MB (52175144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf364f7bc255f1e2a0eb1355b1c840a773629bab59b0b4f2b530783d15a08337`  
		Last Modified: Tue, 18 Nov 2025 06:17:56 GMT  
		Size: 75.5 MB (75513264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7740a2cb9142de24c77416a8bdfa50c8651db10c17e41037dd1ebc15c4e909`  
		Last Modified: Tue, 18 Nov 2025 06:17:51 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:295b9d19108fbb4072d6841c21e6757fae762a23412a20721566a93f91514cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60690c31f3e58f4cacc9bf9cc29d4840c0c2b784b795d6268caca66d8a8b1e22`

```dockerfile
```

-	Layers:
	-	`sha256:7fa1d9f3a121db31010d5a5505b5528d1cb77477abe1e8096d4f3ac34de1ccf3`  
		Last Modified: Tue, 18 Nov 2025 07:49:44 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7e298dfc8764d3fedf84bf1d1e3d9b7b03d4c2e1cfd25e4064a49b0ba13b4f`  
		Last Modified: Tue, 18 Nov 2025 07:49:45 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
