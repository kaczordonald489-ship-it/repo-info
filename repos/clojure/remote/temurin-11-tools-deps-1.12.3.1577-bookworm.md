## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:9b0ffd2fb0f4b41b7fabf85e147dfea474bb3b16cb9ed70a25f6542317a2e40e
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d96759a02b382beee426a01a0661fa0e010a9eaf1309c8fce1ff25cdc320a788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274594817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdd5f30ab0de8823304286a3993c9453e694a34c69387013481aec1feebff61`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:06:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:06:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:06:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:06:38 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:08:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:08:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85bf2bb3f6a55f75d48be786e9872be3a93c93d05d8709dac2645a06118e1fe`  
		Last Modified: Thu, 20 Nov 2025 02:54:52 GMT  
		Size: 145.0 MB (144966634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48975b740c68163acf625d5b77501e3c08302a198cd80aeb7292d0a88d4f0edc`  
		Last Modified: Tue, 18 Nov 2025 06:08:40 GMT  
		Size: 81.1 MB (81146780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4fb17d2f95d67d74b6fefe10d51ba827d37dba46e3ba2c41d4d67e71766b36`  
		Last Modified: Tue, 18 Nov 2025 06:08:30 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b63c2760526d0ab570528b03113f00a59f17121d0604fad06694397444966ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab69d416210f5bcaacb3ec3899e4128e11505feebcd66d061be6dfe5393a2cdc`

```dockerfile
```

-	Layers:
	-	`sha256:28f77d06ad85c7c906048c8ce4e520e37e25a10de0deaf3c90aa8ee7f0de4100`  
		Last Modified: Tue, 18 Nov 2025 07:37:17 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5d382e7fd06f7c22db991c5f1950f54252eeea85daf8b3d248db9babe29c09`  
		Last Modified: Tue, 18 Nov 2025 07:37:18 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5ea8c50521ec24b836a48c7516535d0ea0857fddbaffa5684860464193bb4801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271122242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96eaad7cf92a1a09724e52305d9b76c901c7127139ac7b5720c7e4137653af6a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:58:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:58:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:58:06 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:58:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:58:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:58:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252d6f5be15c22d0d780cac8fa5b09b4773a6c8c9c9bbe94b45e16e5e05fd0b0`  
		Last Modified: Thu, 20 Nov 2025 21:47:48 GMT  
		Size: 141.7 MB (141731502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdab99209c1c26849d692efed7b621671cd5928f033449147968578416c7736`  
		Last Modified: Thu, 20 Nov 2025 21:47:53 GMT  
		Size: 81.0 MB (81030957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7c400b8869f320cc32b5d2240c526e85d5f9c13c6f50fd68c4b307737948bb`  
		Last Modified: Tue, 18 Nov 2025 04:58:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:70d539e649ff1820f1a6338b17c7a39fcc33ea7c12cb331a2b0dc405740bdedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286bc163aa3c15337aec3cdba58bdc71e356d3567af0956e5d97da4b2cfb5d21`

```dockerfile
```

-	Layers:
	-	`sha256:206712e2c30280fa90acb69471e3cadf6af04f2069203e6ac8ed36877ae787bd`  
		Last Modified: Tue, 18 Nov 2025 07:37:24 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38ff868f6f108400e4ea9942a42d02314a53e488c370844e234b8c6e8637b47`  
		Last Modified: Tue, 18 Nov 2025 07:37:24 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:da3223213fbdbdf456f05bcee6a1d5ddcfbcce560bf9797286f7fe5898308619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271395924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19553884cb7053c6df38c3eb72f64d1a8229cec7efb71be83fb43c2356960738`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:18:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:18:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:18:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:18:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:18:27 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:23:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:23:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:23:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764da875785de8387fe160895a48fd21f77d1235503a9bb47628ccbcf6e2015`  
		Last Modified: Tue, 18 Nov 2025 06:19:50 GMT  
		Size: 132.1 MB (132081985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29879b3d82777ee2b8c6f2de4548b17217c501c23a28a9954ea597915a48c8d9`  
		Last Modified: Tue, 18 Nov 2025 06:24:27 GMT  
		Size: 87.0 MB (86986331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215176aeb2f6e35cfef1f42a1e9d90bfd9ac7f0367d4d7115461004c3787af2`  
		Last Modified: Tue, 18 Nov 2025 06:24:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f86b955a8e07bfe142fb8ce84a40fda5164f8c5a4debfbc3b212ef2c3c5037ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3a447ca39ef3ababb307cb8cb2a644670f763d91b9ceb49cc485c9fd82637`

```dockerfile
```

-	Layers:
	-	`sha256:220d08e035f57f01e612f9fc529b410721125e19a4599f9175b52e9fcfd10415`  
		Last Modified: Tue, 18 Nov 2025 07:37:30 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e27b490cb9932050003b2f9a9881702b66aec677d563acc1875b9153981dd08e`  
		Last Modified: Tue, 18 Nov 2025 07:37:31 GMT  
		Size: 14.3 KB (14254 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:2b3a8bc46c1c65fcf8a968022c7c5e947855f4b11fd82e725e6718a2fef2db59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252789394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff0a404ede484dd71a5dc9c57e951726acd9e0b7e04c6e9d353711511bc1ec4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:21:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:21:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:21:46 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:21:46 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:23:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:23:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:23:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74edd87eeef1ca4a456ef8951738a1f7f0691267d689c5317df1e6091dec4952`  
		Last Modified: Tue, 18 Nov 2025 05:22:41 GMT  
		Size: 125.7 MB (125694447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfe2e4f7ae94efc2c12cb9646c53c3d38bdd19581eb4bb22e47cca08e4872ea`  
		Last Modified: Tue, 18 Nov 2025 05:23:51 GMT  
		Size: 80.0 MB (79956662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c419f87f1813544b28191047f24be4831add8c9b64b8481d04db4c5d6432555`  
		Last Modified: Tue, 18 Nov 2025 05:23:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:19a0231a3071e62c9946c56e4b939ee55552a68af259284728cb5780d36011e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe68af97ee035724653b0eb02db7ae7ed0345498b23049c78800c36da8634a4e`

```dockerfile
```

-	Layers:
	-	`sha256:578df3e6e03d53ada76bd80a800895bf849ba0cdbb156b7569e2a29f0c49274a`  
		Last Modified: Tue, 18 Nov 2025 07:37:36 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3f43ffd6bc8147da6564063ecb7cbf7a3e10732b6aef34086b27b010451638`  
		Last Modified: Tue, 18 Nov 2025 07:37:37 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json
