## `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:6ff46fc086c53bbbc62e3fb5f77894ea3e4a2d9874cbbf4a4d043ee372e57d2d
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:084362a9099bd10faa709fd60400bdb6971501f8d57695f0c348be2e8c4f8726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242757414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9a050c9a0f9cc7f2a773bba67e64cb8d0b535de23b3aab05669f8debdde7e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:10:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:10:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:10:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:10:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:10:04 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:10:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:10:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:10:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:10:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:10:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159fcf230eb58fe739c590a3424e4768eb61e57b0c34ebc01e9341df918930a8`  
		Last Modified: Thu, 20 Nov 2025 03:53:28 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c56b7164fe3a3f1a75f1ef0aebcf52b662efc982747c2686b81b0cb5eb4f81a`  
		Last Modified: Tue, 18 Nov 2025 06:10:53 GMT  
		Size: 69.7 MB (69679981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0e515963c041d67d95129e79b73796be4c6bd6000187145821d4857fa8fd1f`  
		Last Modified: Tue, 18 Nov 2025 06:10:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd262b058e2045ec95b51d54d7d3c95729890bc9e6db6e588f41f0135fb2d5a`  
		Last Modified: Tue, 18 Nov 2025 06:10:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27ba7a63b993225fa3cf2e710c7f5bcf77c493cedc2657ff9dedd1c0285bd714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071c61c55ce398cf3bb38a83176930a881d8ccee7ad23a4e6ddd1eb073fb1c6d`

```dockerfile
```

-	Layers:
	-	`sha256:7cc008213c32c303ae3aebd82ac544018638fae24e3ce854683239e4461a5ba6`  
		Last Modified: Tue, 18 Nov 2025 07:40:41 GMT  
		Size: 5.1 MB (5113390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2799da51aea63f610670df07272b5b82eda03cdcb27a0598d3fe3a4f8d99101`  
		Last Modified: Tue, 18 Nov 2025 07:40:42 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d73df85083411e2e2fe4e9a86eec289e08a27440805c2d0f202d203e8a6b3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241343245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99989d1752faa4a3682404fc31871843522dd122b0aed775e02797879017db5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:01:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:01:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:01:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:01:20 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:03:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:03:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:03:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:03:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:03:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f612363b4dbfe909563ce5ee97fdc22ff2865daa8075478a5dd7cb598aea618`  
		Last Modified: Thu, 20 Nov 2025 20:14:05 GMT  
		Size: 143.7 MB (143679886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c9ef5f675b623a1ea85b8263c28e5a81f41c37192c7d3342bdd623c3aa213c`  
		Last Modified: Tue, 18 Nov 2025 05:04:25 GMT  
		Size: 69.6 MB (69560111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9188165fd5be241576c641ed254277783892c070e0a328018b208436c01f5cd`  
		Last Modified: Tue, 18 Nov 2025 05:04:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf66207e0384d2e7f4dbaf23cd6682902f7e840493a891456d9dabafa9b7a74`  
		Last Modified: Tue, 18 Nov 2025 05:04:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e301bdd39c6daf5171f6cbe338466b7bb94ef3bfb105cec3ceb5e011684d4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edecf85003daed2a071fb8031aa880e3db2dfa4b3634a718847b3769b1817df`

```dockerfile
```

-	Layers:
	-	`sha256:794d67a33fcabb97ca5b674b3feb6f31f3d9f0185b694b8ca33ff8835f993312`  
		Last Modified: Tue, 18 Nov 2025 07:40:48 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bafaf5c21d97e14554aaf8df4c0e7cffb5f51741415aba8085e9f8170399c8a2`  
		Last Modified: Tue, 18 Nov 2025 07:40:49 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:60794e6d89c9570eb4fabcfb2ec749e6470e82957b40692d6923803ba729bc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252108437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecc703660d231625ef0c77f045870e46509a540367bd5aa16306a38e8c50ef6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:27:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:27:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:27:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:27:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:27:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:30:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:30:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:30:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:30:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:30:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172e760286a339898f9ca04793550c307642085dbffc819262542c00d0caf079`  
		Last Modified: Tue, 18 Nov 2025 06:28:44 GMT  
		Size: 144.5 MB (144525254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6f37c30fc46c3732ea9de95f46682fb18beb238e010d37ae1210090781b6f0`  
		Last Modified: Tue, 18 Nov 2025 06:31:03 GMT  
		Size: 75.5 MB (75513321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f368de175d375774d3a29ef8b644659143abf6551c53505a672c79de58c8169`  
		Last Modified: Tue, 18 Nov 2025 06:31:00 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f445c0f753495af3d7dc2292010b0c9538f50e3c64046fabc374ed7571022`  
		Last Modified: Tue, 18 Nov 2025 06:30:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3f0f16ad7be3756bd725a225acdc758156824a5a9cca27e5073eac026f6750b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5dd7e77a73df58f1b2a91bc999fa602732feb4dff5f450f5a92bc3017e371f`

```dockerfile
```

-	Layers:
	-	`sha256:5c09b6a8d906e1ed1d040b4976eec274497e709fe1b5813cfde3d1c7129c55fc`  
		Last Modified: Tue, 18 Nov 2025 07:40:54 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1543b222d70cb2cc1da915ff6e930eec052494fa5e2a837ee231c104400e006`  
		Last Modified: Tue, 18 Nov 2025 07:40:55 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:27ad46242f4fc6f4b67fdae172b72fafb43c63f12e1862dbee47e6049f2142e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230235065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16dd6f2302e9a9fc8dcc96a92fd6cdb21f83d263e5495819b9d1269fbdb7620`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:25:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:25:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:25:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:25:49 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:25:49 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:27:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:27:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:27:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:27:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:27:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a11b9c90e42947d63125b1586252482ff242a7c5ee2cff882824559dda83f`  
		Last Modified: Tue, 18 Nov 2025 05:26:37 GMT  
		Size: 134.9 MB (134859061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2095ab49abc4b85ce672a9a3d34100be9c0f8ec9def1fa0e0e4df238e1fcf841`  
		Last Modified: Tue, 18 Nov 2025 05:28:38 GMT  
		Size: 68.5 MB (68490572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df13d0440e8e4f0b8d00e7dd79db5c17c90c3946fa7c9298a3d222994326313f`  
		Last Modified: Tue, 18 Nov 2025 05:28:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eea80d73ea428ab9fac4b75eeecae847ce9090554fd01ef78488dd91c7bd741`  
		Last Modified: Tue, 18 Nov 2025 05:28:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d5b9dbde7ae45908f6a42f15b09285cfb59bebbb5e5749efca0d73cd677f44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9219976e633bb2e3c50a2a6e701b4bbf4d3db9d1201721ff8143fcc3d78729`

```dockerfile
```

-	Layers:
	-	`sha256:e7a329761abc64010d6002ff66e8fbf4e61ff79885beb91405c0a8f5a1a0eea3`  
		Last Modified: Tue, 18 Nov 2025 07:41:00 GMT  
		Size: 5.1 MB (5104711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73f48045c67b86682f66dadc129b6cbbe9b0b0d9a6565f44e7ce5859a4114d6`  
		Last Modified: Tue, 18 Nov 2025 07:41:01 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
