## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:ae258eac8bc82c453e3add0b0af3ba5602ec17785efbda24089bdfd2019b901c
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9c17597b4f9a2daaae0f46893b5e179d02bba1f9f298737ca06e88911efd69d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279682836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2a4f35560389c657ca1d74c125b580e295f3a468cffd74961802ef8d7ec4fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:11:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:11:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:11:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:11:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:11:06 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:11:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:11:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:11:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:11:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:11:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bb15e369205080d76fb08d3b1379cd1cea4a282c7346b244da5ee80938c9d6`  
		Last Modified: Tue, 18 Nov 2025 08:10:46 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e09c89fe070a82e21162bde41a1ffa171b5f3e1cf5fe4b5f24bbb9693f51da`  
		Last Modified: Tue, 18 Nov 2025 06:12:04 GMT  
		Size: 85.5 MB (85544298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfba7706ff06f582806460a56e2e496798da720272ad4bf3a68a1f0b04704a9`  
		Last Modified: Tue, 18 Nov 2025 06:11:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78689ee8871ba5042fb9a241d0dd7d6ead0b1846f18335e82fdd92895e6067ce`  
		Last Modified: Tue, 18 Nov 2025 06:11:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:81091cbd56e045c8bed284b8228108c0201924d6a5c001c5a04436f5c02498f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c32eb8ff34c2d5de4710efac00724ad0bf2e87f6add035958d8dcb5c921794d`

```dockerfile
```

-	Layers:
	-	`sha256:e25edeb4d9f066ec273b75aada99c9858662d923312ef27b342ec9d251b4d691`  
		Last Modified: Tue, 18 Nov 2025 07:42:56 GMT  
		Size: 7.5 MB (7466931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c391798d23ba071e2248e31fa1e8be8358c260c59ca03efacf51c85f616734`  
		Last Modified: Tue, 18 Nov 2025 07:42:56 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:13ff67c08b548a326be8b36fb4ce017c4ab3aef67f032fb8574c82849bc1870a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278696036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc671cc50da154b3d6a5fa7461b20765e4a3facff5c566b493a106669ff5834b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:05:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:05:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:05:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:05:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:05:25 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:05:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:05:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:05:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:05:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:05:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f9ca1dbbcb676cf479b9d9b66a14f666cd14233d6c1c60575eda0e0c6a3ac`  
		Last Modified: Thu, 20 Nov 2025 20:05:31 GMT  
		Size: 143.7 MB (143679909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2085ed3edd0a2ee32ef85266036860d99faa2523f664f1778e02935a8fe470c9`  
		Last Modified: Tue, 18 Nov 2025 05:06:21 GMT  
		Size: 85.4 MB (85364856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931e72fdb0cdaa4fbae8b2eea30367ccd5ab1b7ffb2c0dd4e9c3c26c6d70beb8`  
		Last Modified: Tue, 18 Nov 2025 05:06:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c375e7a4cb11d7b5c72a2c0930480748d4c8c1c59160bd63bc82fab302bb62`  
		Last Modified: Tue, 18 Nov 2025 05:06:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ffe3d442dfaf577ba3bd4400ee516f04717327fd1e7c1d2f19286a4ae26b6853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1d093af75fcf67c9fc1cb841e0e5089dcfe795503650de2fabf4c4855981eb`

```dockerfile
```

-	Layers:
	-	`sha256:d49f4635dbe925c4bea7205264569050352f910ac9a8c2dab2d9571fccd284ae`  
		Last Modified: Tue, 18 Nov 2025 07:43:03 GMT  
		Size: 7.5 MB (7473961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4549d90926294aec1789a4962951d5777594f101aeea654c4fe45a00ec0aa28e`  
		Last Modified: Tue, 18 Nov 2025 07:43:03 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c50fd5f380d78054e7e5cf7e230d1fa8178f5e4665f17733ea8393cfc87bc448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288582163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad389c30c7a431b60884999359613447b7acff5926998bf6c7badfc67f42fedc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
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
# Tue, 18 Nov 2025 06:32:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:32:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:32:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:32:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:32:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da80b0b7e9cdabab99dc7af0f635af96aacedb4c191f0957db1f4d6088c8548d`  
		Last Modified: Tue, 18 Nov 2025 06:28:53 GMT  
		Size: 144.5 MB (144525203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61556131f2deb7cdd0bae5fc10ef79b22c52577d6cae2a19b419178e116b14c`  
		Last Modified: Tue, 18 Nov 2025 06:33:45 GMT  
		Size: 90.9 MB (90947437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e037ea451d43447cc7311e06ceef2f90e568aeba206fb4ce237fae73bff9df`  
		Last Modified: Tue, 18 Nov 2025 06:33:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3735947d4281be7fa5b0b0565b2bf87d03109aa6f1bc3dbada0a5e406e3263da`  
		Last Modified: Tue, 18 Nov 2025 06:33:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d7b2964d67ac396b6324b8ed7f7c0005dbbb5b422a8701c766ce2e46bce4611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44258decf7db495f4f0e7b510af8f0d844c6bce6f6598c10f5ef2adc91a8fc1`

```dockerfile
```

-	Layers:
	-	`sha256:b2d83f1a1b50a7b246b0799190d1b93d5fd090f5c4396b40286ed7ecd671d64a`  
		Last Modified: Tue, 18 Nov 2025 07:43:09 GMT  
		Size: 7.5 MB (7471350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2602931e7c4b96e1bf9273c2115224aaf2539a678c0101def569794700078c6d`  
		Last Modified: Tue, 18 Nov 2025 07:43:10 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:07f420a77124437113d5cf094c73593e96f585d9f946caf614291dec94ea70a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274088332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203cd3a413686e89de16e97a57b38b76c8327a9cfe47952bbcdd1d5674ab33c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 17:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 17:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:51:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 17:51:25 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:07:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:07:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:07:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:07:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:07:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c945a137e71885488da7cf422518c6c6ad2c6a58a7c3ce93e4735ec87fbd338`  
		Last Modified: Thu, 20 Nov 2025 18:04:59 GMT  
		Size: 141.9 MB (141889553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051c30ac1da2498ce7c09ebf1bd8a6acb13765e1d1ff92fa2e5848b61113d187`  
		Last Modified: Thu, 20 Nov 2025 18:12:07 GMT  
		Size: 84.4 MB (84426542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf04e5470279dc2a1aa5777505f008ed2a82ee2dc04081c02e6498ecc3e6f8c`  
		Last Modified: Thu, 20 Nov 2025 18:12:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327d4047439b3c12ffe462a1b334faff84163e3bf6cfc1141181f2bf2539a998`  
		Last Modified: Thu, 20 Nov 2025 18:12:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:381476698a4d2d2193522f225f7af9ba2e8a84bf21a5d051c491489920731b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe156463cb159b1eec24b16e588817284a51b1e3c8fca251df39791066fa2266`

```dockerfile
```

-	Layers:
	-	`sha256:ee377d308003b3cc7c9c1a8e20a97ef7884c31aaf99bbb068afa78107cc7e60f`  
		Last Modified: Thu, 20 Nov 2025 19:36:09 GMT  
		Size: 7.5 MB (7452925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88d08502be1e6e5c62d0317c1894b90e1a8548de594ddaa3bd5ecea8126b243`  
		Last Modified: Thu, 20 Nov 2025 19:36:10 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:386fb5ff5b2cd01b723abab2aeddff7f191725768c2b93c945a85168f31d63c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270717476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914d91c7965156d78be69e828aebeab179611d8c84207dcd36e636650bccfafa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:27:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:27:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:27:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:27:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:27:31 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:27:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:27:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:27:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:27:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:27:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c1e959aef809914c50d553c82ad0d185252102b0b672180fa9a330ebd82b21`  
		Last Modified: Tue, 18 Nov 2025 05:28:31 GMT  
		Size: 134.9 MB (134859047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b68e596dd64ff1a31cf3736bb8cfcd03d041799df8e201e91fffcf77fc7049`  
		Last Modified: Tue, 18 Nov 2025 05:28:43 GMT  
		Size: 86.5 MB (86511373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7ceb58365c3791d3f10bcce58dcd537060ccec9d1c0c7d79c826abb499b5ac`  
		Last Modified: Tue, 18 Nov 2025 05:28:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe7d7ca0f41476ef3d330876e505e2385345e4127e11affaeb1d518f3e5666c`  
		Last Modified: Tue, 18 Nov 2025 05:28:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2a1333a97faa8855aaf1a7d732ad87d3cbbb67cd8a61153b312da2a908fcf6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ee0106131fa4e47c0e4164ff3361e30406327788c513d940a47985bac0e829`

```dockerfile
```

-	Layers:
	-	`sha256:4a0fa42d0127b929233c32f40ac3998a0f8546bdea17676d39f2348c6816455b`  
		Last Modified: Tue, 18 Nov 2025 07:43:24 GMT  
		Size: 7.5 MB (7462853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0997402b2ff824ba0bc297bfd7028b8007c20b125ee1cbc11c9bb0c50debb6b9`  
		Last Modified: Tue, 18 Nov 2025 07:43:25 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
