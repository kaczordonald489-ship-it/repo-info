## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:2d799c64f5eb428b67dac8d207c895d31516e6c950192e8a297d2316bc128815
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

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:95dd0b695f0b8eaf5c389441cce174f98961a12be095660f8534529333817a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226877165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552d37d987ef035f46a60581bf196bceedbbd903061e812289062107dc82020f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:18:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:18:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:18:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:18:08 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:18:08 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:18:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:18:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:18:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:18:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:18:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397ad6b02b04c0fd125b32ee2a29a3d6d048995d4ec58929224cc6b667743e1`  
		Last Modified: Tue, 18 Nov 2025 06:19:03 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764864c0142f65dc918c15f343724e268cb3e125b66acdad82748b204da4e15`  
		Last Modified: Tue, 18 Nov 2025 06:19:01 GMT  
		Size: 85.5 MB (85541279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b22e5d52250413781311dd6c97c283483d06b41be3ac8ead7704f7a7eb72b0`  
		Last Modified: Tue, 18 Nov 2025 06:18:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83093ad96921338bf27da9d0e1b36a20166af05d4feadad73d9a640bc8443dd0`  
		Last Modified: Tue, 18 Nov 2025 06:18:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:72e813a53cc76549047393841d2da7f3baa3975c9a42c13d33480a4bf471a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385017474cddd422209d4415f8fca350070e9a15a38931b766d6b8c430a65abc`

```dockerfile
```

-	Layers:
	-	`sha256:27c7d72fe366f4e795860ed377b10b86e1a4c766ad15252f9a785651d611b648`  
		Last Modified: Tue, 18 Nov 2025 07:48:36 GMT  
		Size: 7.4 MB (7418261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c70b1b584b12d0c4de0ddb059d434fd3fc6f4577bb3786da1cdf7f6a57aea6`  
		Last Modified: Tue, 18 Nov 2025 07:48:37 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83a1292a7b9e10967946b25eb9220ad8bfcbbf23705670bb8fae8ff85ab18ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226068448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e85514eadc5a1cbf3077bc20aed88169354e15eb9f97389af0ef51b0df089c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:13:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:13:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:13:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:13:46 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:13:46 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:16:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:16:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a34b5239753bd9abb4f6cdf7dcfcb68d31fcde530e94e8c07ef9debf944139`  
		Last Modified: Tue, 18 Nov 2025 05:14:37 GMT  
		Size: 91.1 MB (91052512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c6a481379f00fdee82352ade17eb7bd1165eee498c40bd19ee7c160bd7a05`  
		Last Modified: Tue, 18 Nov 2025 05:17:20 GMT  
		Size: 85.4 MB (85364665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf597183086db77d7f11ac7d51b453207d971851573f0da087f9a73d88027d3`  
		Last Modified: Tue, 18 Nov 2025 05:17:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c68720bbf97ea447bc5ce914ed82aa3856855bac41fc73b1d0ea998a2302f0`  
		Last Modified: Tue, 18 Nov 2025 05:17:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6d0e1c79bc201c31b929db534ddba68aea39d0d50a8feeff7611ddd691213a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc67d7919181451e25f0bcc8f292ab5924b4924462c52afc7b7eeec3bde68333`

```dockerfile
```

-	Layers:
	-	`sha256:94deac09332c216d1a3c97df0bcd5241f6a52fcc69586d84e52e4be89aa3a76a`  
		Last Modified: Tue, 18 Nov 2025 07:48:43 GMT  
		Size: 7.4 MB (7425312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8245850f684ce543b32e8eb5cb55f2867854115808b29b5e914fa328b31f558d`  
		Last Modified: Tue, 18 Nov 2025 07:48:44 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ef7b5d22836cf048ea7161488e924a8d62a18f022adc0638da9f18b285a6a1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235667699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20441df84f249cd5d0e1858b6a3ce52299b507a91891e1423796e4f5811b7078`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:41:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:41:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:41:16 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:41:17 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:44:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:44:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:44:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:44:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:44:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9af0794116b59f75955358fb63fbfaa3b3dbe4c37312d256c3296d2bbd7e31`  
		Last Modified: Tue, 18 Nov 2025 06:42:55 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459c3c9325f01f1bb10dd305804ad76a6f0e9c1cd332ccebfc4e16a3162d2c5`  
		Last Modified: Tue, 18 Nov 2025 06:45:34 GMT  
		Size: 90.9 MB (90947427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40220568915ca8bf66fa13fa99ba9dd0fe0e70fe9cd32b590d1e4bbb3e85321a`  
		Last Modified: Tue, 18 Nov 2025 06:45:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47b9c8f418b52744cdc0bb2e5ede9b3f7dcf6df472d4ca1dd5d88c2ca4c1ab6`  
		Last Modified: Tue, 18 Nov 2025 06:45:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3bae5842fb237d63432dd68e46c36ba3624dc51b986841aee8d3650f534f0dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b20a23ad5c12dd6432bbb62ce37252ca7d4c57f88e5360c2370f26a350c5fc`

```dockerfile
```

-	Layers:
	-	`sha256:f4db965eaa129d0b708d00a5efd0d3603fb6b5a8b3eaf64e2b9e58c891e950d5`  
		Last Modified: Tue, 18 Nov 2025 07:48:50 GMT  
		Size: 7.4 MB (7423990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b20e68c1a1e55b7cd640a6f2d30989e4a989727324d64a8bc4aa130893cdb6`  
		Last Modified: Tue, 18 Nov 2025 07:48:51 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:95373b1751fa6df9cc8c5c3d811d2340462011cff62d780ba74001f7104a2c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222951802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28c36a8b3014591b5b2a5c1ef73d986034065812f09ba38b057b8126ebc3add`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:48:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:48:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:48:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:48:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:48:04 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 19:02:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 19:02:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 19:02:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 19:02:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 19:02:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82da52be06de4ed4999d84e1a9d7d08b95b3d6f3efeae3a90908819ba167244`  
		Last Modified: Thu, 20 Nov 2025 18:54:07 GMT  
		Size: 90.8 MB (90752860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d96c70020c6aa81739134652887b2145444376e667c11fc82664345551ff81`  
		Last Modified: Thu, 20 Nov 2025 19:07:05 GMT  
		Size: 84.4 MB (84426704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aef4b5f7446ed29d2e9fda0674fc7bc52e1d0b3ff910603fcccf362ebce36d8`  
		Last Modified: Thu, 20 Nov 2025 19:06:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c31909422f581587106903a38bf443decdd9cebcc98f7f694eaffcbaa8316c6`  
		Last Modified: Thu, 20 Nov 2025 19:06:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:379c85f0a41d7336bd4e08e7807b5fe404a446e577ba2ed1f5955369370727bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6992f64947961d74feb6d6c69372c2e4d1bb3db0e87d3002ff6a458c5f66cd`

```dockerfile
```

-	Layers:
	-	`sha256:460a0fe54f4bda90344f8f6324d13c9c979feb1274bce9cba722f21cfb291fdf`  
		Last Modified: Thu, 20 Nov 2025 19:38:24 GMT  
		Size: 7.4 MB (7406183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160a0fe166c8a23ca505fce98860fdc430103e5113655e3eea9e5b463009b6e8`  
		Last Modified: Thu, 20 Nov 2025 19:38:26 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:66895a40ae7040f6ad3ed11e76707c1a7074e9bbe8ed1cd3b69c6e03d1369fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224069101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e52ded659d729ef2051e2959ea8b7137dbba8c5c5c33584c2569eda8e897fd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:33:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:33:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:33:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:33:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:33:16 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:33:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:33:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:33:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:33:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:33:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8379765f3f10db78b16a36f85c3be0c8bbb9203ce97e5b395260090c52be7ae2`  
		Last Modified: Tue, 18 Nov 2025 05:34:24 GMT  
		Size: 88.2 MB (88210703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37db7f8e19786ae8a4d0491193d386eed1eca7d0f5c95bb016762a05a1409b0`  
		Last Modified: Tue, 18 Nov 2025 05:34:27 GMT  
		Size: 86.5 MB (86511344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a891ad704e910c12c7299073d3305750a7220b1b54a94ba91297e3d35d91dc`  
		Last Modified: Tue, 18 Nov 2025 05:34:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ef1f38eac99c96eef8e316dfc0128af4ad1fa2467b228128dedb1d1bf94ad6`  
		Last Modified: Tue, 18 Nov 2025 05:34:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:be76984abf500fa8c71df1c86a2afafeec9c2c4f57c82a10a1c24256467e2da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca13dd3d3c775ccfedeeabb7ba70194a7e0c085b7e8e15602f2263edfafa6630`

```dockerfile
```

-	Layers:
	-	`sha256:ec665d761c6ec24341cff9e99785760d8dea59186b6f07d2be1bfc9f2ac831c7`  
		Last Modified: Tue, 18 Nov 2025 07:49:00 GMT  
		Size: 7.4 MB (7416731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253a3b32df9067f884bc982b196608815e3e987ae035bfb40e23a4f6b74a0250`  
		Last Modified: Tue, 18 Nov 2025 07:49:01 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
