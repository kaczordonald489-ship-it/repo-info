## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:b59abccbeb92ffebb5565c010f84639df5d16a0a82bcf54b72ec8decfcffdff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b263277053601370a4292af0811136d29deeb7f959b935cd9431e4c216b354f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246620891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a921faa21194be6625809a893b903e9c1ec1f3fb1223e90fb130500e43148b91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:11:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:11:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:11:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:11:09 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:11:09 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:11:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:11:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:11:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:11:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:11:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5969a2ed82f25770a91b15ede8fd8798afe66ed20862902271e3ee216d3e4`  
		Last Modified: Wed, 19 Nov 2025 22:14:27 GMT  
		Size: 144.8 MB (144847975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42b5e378441f1c7e611cc459917cb579b9e7ddd816d2a741b47f78e88b95e01`  
		Last Modified: Tue, 18 Nov 2025 06:12:02 GMT  
		Size: 72.0 MB (71995389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce54ca4f7a585e4574475d88ff73a27db17a57f991493b96986a36b43b8e86d`  
		Last Modified: Tue, 18 Nov 2025 06:11:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a6b72c36353c9d5c0da02eba82852cc24cfb3ef5ea968260c0484714478f1b`  
		Last Modified: Tue, 18 Nov 2025 06:11:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db55a513ecf3e3bb1579a01bbb69d3c50e08a67aa9bc8f5152caf7ec00b4d4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3864550a04e46bf7cc05ed1ef3ca55d59aaec98df36523980825dc11652836`

```dockerfile
```

-	Layers:
	-	`sha256:4c670694d54d779937788ad158a010306751659c6b6222b348bb9c48ef736030`  
		Last Modified: Tue, 18 Nov 2025 07:43:07 GMT  
		Size: 5.3 MB (5256199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e80e4764f41a091f63af3ef1b99612d1de1cb85d2a430bf2b5cafb4e5c89bc`  
		Last Modified: Tue, 18 Nov 2025 07:43:08 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e9004cf3de452b0ec54ddd3e38a7cd8a9722d337255eb5f00444a345c7096f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245628040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226e7d4ff65be0b8c04b541055011c0981471c4bce3ee8e16c99b97c1499ee41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:05:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:05:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:05:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:05:24 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:05:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:05:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:05:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:05:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:05:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967dd387a1ba781240fae3560d34eab254c38e119ff41f5ce7032b966d47ce3d`  
		Last Modified: Wed, 19 Nov 2025 22:15:15 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab2155ab85675e4c9bb67816d5589013a981e1368440e4a48b10554c974eea8`  
		Last Modified: Tue, 18 Nov 2025 05:06:18 GMT  
		Size: 71.8 MB (71808468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145361a0925c8106cb4b40c4a3c2ae16793a5bea58bc49e6d389a29f8e6a0317`  
		Last Modified: Tue, 18 Nov 2025 05:06:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4d02cf0d9ee34e792bbcd505bd1d16e7298373cf850619959909911371604e`  
		Last Modified: Tue, 18 Nov 2025 05:06:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5ad3a9f1be10ca9bebeb850d50a5b56117661a7fa03825905b5f98304e48950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72571211cc875d6e5a25b7d4750d3921282a02adf853209c9228e7226634671d`

```dockerfile
```

-	Layers:
	-	`sha256:ef519995367563942297670773e3de47f4eada5225befd887f7fc5209748c641`  
		Last Modified: Tue, 18 Nov 2025 07:43:13 GMT  
		Size: 5.3 MB (5261968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98685ad0b20b4d95555312dc72d46e6aeeccd9448b58e46aae72381a5c462f6`  
		Last Modified: Tue, 18 Nov 2025 07:43:14 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d8e65c98d56bd75cb0a8702e84e4d7beffbf88705e045b8721f65b02bcc628af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255514353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b9c089de1bbc595306c4cf29a122a71c7c45cd8c76074134827598aa909fee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:18:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:18:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:18:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Wed, 19 Nov 2025 01:18:07 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:18:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Nov 2025 01:18:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Nov 2025 01:18:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Nov 2025 01:18:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Nov 2025 01:18:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7265887b1da4e953ccb001f192116d1c869d3152ace48f57d173138e0502273d`  
		Last Modified: Mon, 24 Nov 2025 10:02:24 GMT  
		Size: 144.5 MB (144525202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0725b7ba2628d2d2aecbb197f7eee8f77eaca1f389963b0b12dca0558a7eb8a`  
		Last Modified: Wed, 19 Nov 2025 01:20:12 GMT  
		Size: 77.4 MB (77391252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db578b4d4f599e2197c872fec5133079537438b9a62af23c54c2ae2b3be6a2`  
		Last Modified: Wed, 19 Nov 2025 01:20:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51661b324109911024e4df462632ca129e89cd591c605d43dd3be30e6345dcc1`  
		Last Modified: Wed, 19 Nov 2025 01:20:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8266369075db5521c144e888d520cd7538fa8f8d542a552a78a5944fc0e82723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea4d2426c4c4b8aee6b7c7ad21155afe4754ff57e09eeb884607979a42dc15`

```dockerfile
```

-	Layers:
	-	`sha256:54e0b01ba04dd6aeb95cf6c8bc6497b4cad280d9f8906ea71b93ab0e624a0f14`  
		Last Modified: Wed, 19 Nov 2025 04:35:46 GMT  
		Size: 5.3 MB (5260570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e8363556dfa1df9693927a8aa777dface7d4742f5ded2415ad70fc76afc1ef`  
		Last Modified: Wed, 19 Nov 2025 04:35:47 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b7fcba47385387d2f5025ff51c69567048200b21752b07cb61600f11bfd779b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241044426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8b9ee9db7c2d983773340998002aba044d39a901b71b844d94791f1fe8b38c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 17:58:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 17:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:58:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 17:58:06 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:15:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:15:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:15:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:15:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:15:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d74684f217d805ec7013972d089a9baa3e158cc8603592f0e9ad77ff195488`  
		Last Modified: Mon, 24 Nov 2025 10:03:10 GMT  
		Size: 141.9 MB (141889576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eea98d77616be41c09934cb46b70eba0ca9ab138e93b4ee6b79fa3e83b2662`  
		Last Modified: Thu, 20 Nov 2025 18:19:35 GMT  
		Size: 70.9 MB (70880679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c914af89d78b8885c7b112dde37fb3caf15da1ea18b890f10f7427d6d49220f`  
		Last Modified: Thu, 20 Nov 2025 18:19:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600638db24b8bbcdb7a9b56b79196800ce0dd63d4d39eb5d7af6728f79c8aed4`  
		Last Modified: Thu, 20 Nov 2025 18:19:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:090c80513ed6d785f23be04dd755b76efca95a75d03188a084e89a2235385ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e819d5cfed22a7b5148e52714b7521ec2b6c2c24f69fc8d1fbee67f9179416`

```dockerfile
```

-	Layers:
	-	`sha256:25a4538fe012ce286c44205ea66e598f405ab3c5ba93672f5d215bf19af20da6`  
		Last Modified: Thu, 20 Nov 2025 19:36:14 GMT  
		Size: 5.2 MB (5243744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f0a97c28cdb53e71d158f3ef847b637125036ed5d3394e252cff9786be2328`  
		Last Modified: Thu, 20 Nov 2025 19:36:15 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5a0f2dedda69e6ecde6afd99ff5d2bc3cb54dbe4f40a86b73c7c86d8dafca44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237648196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8149fe8b68a155855ffca18edaae36bd19bb813022553a2d266c378342c81e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:27:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:27:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:27:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:27:33 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:27:34 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:28:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:28:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:28:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:28:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:28:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c147134912bcb5f024fd99ef3a8779bcbb0eaf98fadaaeddd35e58397454d65`  
		Last Modified: Mon, 24 Nov 2025 10:03:53 GMT  
		Size: 134.9 MB (134859047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e89fec891ce4efb45df55fdbdbb1d4aa03a483dc5a1b77b67a2c5ac4eb8e9e`  
		Last Modified: Tue, 18 Nov 2025 05:28:52 GMT  
		Size: 73.0 MB (72953743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d50505350006edfbe2b07fa5746542fcd5a2b347566da306bc67742822e8c25`  
		Last Modified: Tue, 18 Nov 2025 05:28:42 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df3b4bf49b755637651d121d813cd6690786d8b515c02f5977d19445b9b88c`  
		Last Modified: Tue, 18 Nov 2025 05:28:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba644c7a8e7e5cddea3bed6eb4d02013d94067df25d0f3601bf476f3ede2db7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0db50dda8dc0063b8d90b72298bebf979c922d038e227904ed0fba64540725e`

```dockerfile
```

-	Layers:
	-	`sha256:4b6ce650e410c211aebe03377846fe86c3c5401151c63e06687d0d8c89ad1165`  
		Last Modified: Tue, 18 Nov 2025 07:43:25 GMT  
		Size: 5.3 MB (5252123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e408cba8881c80c767b3b497cf3552460e80cb68ba9f15d2b3c7bd90c6746f0`  
		Last Modified: Tue, 18 Nov 2025 07:43:26 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
