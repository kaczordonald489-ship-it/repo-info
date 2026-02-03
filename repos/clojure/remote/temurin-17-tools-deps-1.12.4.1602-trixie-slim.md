## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:78a427dda88a148fbcc4ace594c7351758d9fc693619889543ac13f19e1d6683
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0f6ca230c5681c7fea30c4bd67033335ec45b9f627b9c0b42e48234ad8d91b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246623453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639f449bcc12007c395b7cc16917c2332ff6458b435954ad00c8f8935272ac17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:56 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13751002ea93c7f5d9471794f7c72a340559d518586756f0f8bb47a014eedac7`  
		Last Modified: Tue, 03 Feb 2026 03:21:37 GMT  
		Size: 144.8 MB (144847923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72371970a21f9faa974851298cea88d920bb4f8e329b6f5814d4b737767722d6`  
		Last Modified: Tue, 03 Feb 2026 03:21:35 GMT  
		Size: 72.0 MB (71995891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d921436da1fe01a2eeade94980682fc291c4ade8027b5e681c9cd256dbadba`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a2d44842f4ed358e144c04e683582204bdbc84a73c890539abd28b72783c1`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6a3ce3f84bab79e1737456b0abe5be8fc12e11b1e2f39e93e25f81ad41d7121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f063048f36d277d4ac297f5d819acc2218da0860924261f75e9dfa4a6785db3`

```dockerfile
```

-	Layers:
	-	`sha256:3c95bc33f14af38988ed0955d57a34b2f6af67ff834b1e07d1d5a08972b6a214`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 5.3 MB (5256299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6328061c634cd3a4214b2962bb0d50b2738e95cd2e0a90d025cdbc21bb48c7f1`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e71b57e7c76c7a9d6b4b3d0bcb34964c944eac7a30399306db1379cbbb74074c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245627505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7312c24de04e27ac6aa692248c7b9708eb8cb9d0ab6927e4fbfbdfc853567188`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:35 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9decbf06df2ed49493df0faa0cb65fbda5284c41076ede3493bc5ab70fa96934`  
		Last Modified: Tue, 03 Feb 2026 03:24:14 GMT  
		Size: 143.7 MB (143679921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3485f74eb68e1d9ddad3b1ae5abe91cd74d9e5cfa4632b27d791e22eb3345c41`  
		Last Modified: Tue, 03 Feb 2026 03:24:13 GMT  
		Size: 71.8 MB (71806478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cec3c89ad5c4d5f40a1cab9bb66681582f38c9dcce6818c93b3f7d6a1f61c42`  
		Last Modified: Tue, 03 Feb 2026 03:24:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b168b6807d88e03b6fa3f8329befd10423fa2e640cbf5a14d9e3f0469820f913`  
		Last Modified: Tue, 03 Feb 2026 03:24:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d5ce921d442918548d266b9efa264e5e9868487935a0a6e282361165b2fce0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a7ba543d245dd2def69b96e29df9ec93336cc83fa1063bf605333bb37b7bed`

```dockerfile
```

-	Layers:
	-	`sha256:7471540fa7322a95bd6355bfd0a108d58ddf0d7c40ec9baea9a49c1a0494701b`  
		Last Modified: Tue, 03 Feb 2026 03:24:10 GMT  
		Size: 5.3 MB (5262068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d27b7e281c24328db5e6305607dd8d98f1cb536cee424cd999b8bf128aa7bca`  
		Last Modified: Tue, 03 Feb 2026 03:24:09 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:073215bc499ea8db419f891e8e564462e4346dc6b66e838c98b18e7ef0b59827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258712013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d04a8846aa3e01c2bb14dfcf43a25ab9a34d819025130b9e2eaf760fbebcd23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:26:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:26:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:26:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:26:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:26:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:26:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:26:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:26:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:26:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:26:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7f3b48545bb26df22f8fc2393ea26e698fcaf9b03a0325d1f54c82ad63d640`  
		Last Modified: Wed, 28 Jan 2026 18:27:38 GMT  
		Size: 144.5 MB (144524726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4371e7d439aaeee5763724cfe6ca662ba97c39273e7a322c77140016ba94997`  
		Last Modified: Wed, 28 Jan 2026 18:27:37 GMT  
		Size: 80.6 MB (80590643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318373384cd2854e885994cdf90a78546a366b51f43278ea2d1216910580612`  
		Last Modified: Wed, 28 Jan 2026 18:27:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afa899bcea092352d79e4473b3f2a4607fe60ab567fbd9bf0940e02dd79d79`  
		Last Modified: Wed, 28 Jan 2026 18:27:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf60d51b876dd3f0fe33c3bbef4d0d5376bffa7bb4fc55a93c2a5712c065091b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7869ac237e0088480d2cee86ad5e59d8400d30aed2d8782a4f94c772cf8446ff`

```dockerfile
```

-	Layers:
	-	`sha256:91d1ceca2a2410d4db48665ec082794279c5920d673b6f4e3c1255b64c01879a`  
		Last Modified: Wed, 28 Jan 2026 18:27:34 GMT  
		Size: 5.3 MB (5260670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330cb8ff7feaf0eca2842c20ef2f55bed2c55757ced61171c1f46257f3488eae`  
		Last Modified: Wed, 28 Jan 2026 18:27:33 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2fb2ad760c0d164a7f21808dcb461fd6e9e81fb66a7eeb49753c525763ff50e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237651889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f2094ce4e78c1f13383e9a8ff15f58abc5fb91b58d212c6c92fe0c327ec469`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:03:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:03:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:03:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:03:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:03:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:04:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:04:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:04:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:04:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:04:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfbbdfe36872be683d507789f5d9f57b4472fe24b0ff3c3fcff320cbf2dab54`  
		Last Modified: Tue, 03 Feb 2026 05:04:30 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ac5c3b9c02c293325a36a6c76f0643c8ceb48134fbead6bc72a72712efa17e`  
		Last Modified: Tue, 03 Feb 2026 05:04:29 GMT  
		Size: 73.0 MB (72952925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9dfe488758086592fcd6462a057d4fc10ce551c1f73ca666ac1453c9db7b88`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ae76bb7ca089e43d100fa901b51f0f04fc967d3b219a5e9effe5a8d9c3b338`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02b9c0346418cd4f32cbdf2828a77ebdd4fa1173fe5b139eb6fdc1803639b985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2922934d66f72a814683e2305bcb95b2e9708cbad159fd2038e4fc1a4c01d7b2`

```dockerfile
```

-	Layers:
	-	`sha256:d65849885d8c575a421460525686d153bc7c30d5d1e00fe4c856c0091e302348`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 5.3 MB (5252223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922c849c6eed3bd20161705a99987f5c2addc19396b64bf109c70f4b1edf0fb8`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
