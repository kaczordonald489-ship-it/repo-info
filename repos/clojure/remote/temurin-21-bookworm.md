## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:5c9fa6f135460a6afde686e1dc76104b0c67e930636d470231eb1817c2961a3a
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

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:78b8f8dddd4da5f37698ba20924696c9e53ffdeb20be6f3511db545218ae231a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287453705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a769fdf1ae392007fb164e2380acf98240d1a0a6bf2377c65a827dd6213804`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:13:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:13:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:13:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:13:13 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:13:13 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:13:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:13:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:13:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:13:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:13:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c297ee0e60c726f227fd140b61949bff70241196084ce3c075712b5ba2784dd1`  
		Last Modified: Tue, 18 Nov 2025 08:00:53 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3bdfad89e5df17cc98079043750b4a5e4fe7c8be2845999456079896c25855`  
		Last Modified: Tue, 18 Nov 2025 06:14:12 GMT  
		Size: 81.1 MB (81145874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e54ecb2f590d7351719b202f7bb8ff93b8bbf1543ee9d505ff6f1e54f74df`  
		Last Modified: Tue, 18 Nov 2025 06:14:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155ebe15b68fb3a8423b8ee8b2a104fbb81a18063742b75d6d702f0a969cb600`  
		Last Modified: Tue, 18 Nov 2025 06:14:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e57b81f846e0645dcbadbadb64e5999fa49a60ba0579ab93dd5e1efe0296ae8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895c5a76537da7677de22d73e2b2e9c8e8d34953c889982d3815d0cb43db9dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6d6450e4e04d7b8fd15f6fc0a6ab3579713ff7fa13a6e61ba9308d19fe3c5470`  
		Last Modified: Tue, 18 Nov 2025 07:43:47 GMT  
		Size: 7.4 MB (7378678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929f7492f665ef93d9404f74e99364f5a1729bd7bf20c34fbdee16a763de53e4`  
		Last Modified: Tue, 18 Nov 2025 07:43:48 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:91dedfc0dbadd25ab464f15ec0f425a020ecaa8486f092e2405f9f70ac04f302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285498365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfd25971c3553deb38f23835b0bade20decc40ceacf3a395c344ec2617fcdab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:08:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:08:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:08:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:08:51 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:09:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:09:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:09:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:09:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:09:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b594ab18655e5796592de2c5d08f8caae880fa73e33598dea547bd99e164dc9`  
		Last Modified: Tue, 18 Nov 2025 08:04:29 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04775b6594883ddf933c2e18c2b63fa702a9c224c7a429dc326a09781027d9aa`  
		Last Modified: Tue, 18 Nov 2025 05:09:42 GMT  
		Size: 81.0 MB (81030537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448235a014b5a5a27554b7e100eba92a79318ccfe7aee6c8d6744f9b46438853`  
		Last Modified: Tue, 18 Nov 2025 05:09:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac02d27b7818971b2bab0ec5f9946264b48509d211d524337de09c698a4890a8`  
		Last Modified: Tue, 18 Nov 2025 05:09:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8570c9d9f2f2d8ba997471663dd17f66da086b4548aab6d113a08ce682df1afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c91b1373409e15091afd10120d09b565e0d2943bcc78d2d913533e024b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:e2c068da2a202441470404d6a9f8275c9744d2b5bfca9984f224e4c36618f21f`  
		Last Modified: Tue, 18 Nov 2025 07:43:52 GMT  
		Size: 7.4 MB (7384465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ad0295e4019b51c2b29b22fa7473872238665e85ed86ffb4e8699db46bfa9b`  
		Last Modified: Tue, 18 Nov 2025 07:43:53 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:78da4a2a94c26e7f52037bf4747d6fb1c580b0ec5b512b8190dd520fd5d9bc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297257029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc74cfe552d434012ff802c3182442ac510280b16f4f52f7aa355875ef8c912`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:31:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:31:45 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:31:45 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:37:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d206fc81389c537bf3bf40e30bcd9d24259322fc1603ad6f79f10d5009db2a`  
		Last Modified: Tue, 18 Nov 2025 08:05:04 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776b3f14a6c5bb09476f7188797fff275a8e5bbdfe7377f37d2abbd82474b86c`  
		Last Modified: Tue, 18 Nov 2025 06:38:43 GMT  
		Size: 87.0 MB (86986086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3a6ddc1e6ca8ae04ee60c272bd95f81bff6eb0c1ad4de317caed5f05009112`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42fd48ef98b4316abf4715849e8f518402e4cb671cda3a5a0eb7e84c0e9fcd`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:524b85ca865022d7f854f6f75d4ef02ae8c446e216753c49dd50d436896b6b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d316a7893a03c76832a5b112cc3b7d1c0880c9979f8b5571a99b9d38a6c3e7aa`

```dockerfile
```

-	Layers:
	-	`sha256:827685af0bce9ba904ee0ad3ef5cb12c512f0722e24d70a67c52e4282a4213d0`  
		Last Modified: Tue, 18 Nov 2025 07:43:58 GMT  
		Size: 7.4 MB (7383904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56ac273f38e8e0169d22d806c5f26c4e093facfabce046858633e77228771ab`  
		Last Modified: Tue, 18 Nov 2025 07:43:59 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:01854e7e118d1c95485c87c06406c1649709e582aaea0c39f348404d1466e4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274165035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee18f92d288197793f41d6f69aca22775721264c179d1a9a6826ac7eb0d78914`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:27:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:27:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:27:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:27:33 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:27:33 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:29:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:29:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:29:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:29:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:29:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a4c2d7559d27df7dde4cd8b1f0f676863b5a0c885adc1250cf0bad409e4500`  
		Last Modified: Tue, 18 Nov 2025 08:05:38 GMT  
		Size: 147.1 MB (147069839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a25693b88ffc9aae1f912538b269086e17fdd9fe1a5c1d7616dfa70b39de379`  
		Last Modified: Tue, 18 Nov 2025 05:30:28 GMT  
		Size: 80.0 MB (79956514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9bdc8fd6ed5a5efc55af72734ed03e4fe8d548adb3fc4e6ac4275faf342ba0`  
		Last Modified: Tue, 18 Nov 2025 05:30:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefc7721c9f32ad6c52f7c9e2a831960b767d81a16135cac846bc1dfb6211b93`  
		Last Modified: Tue, 18 Nov 2025 05:30:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b914a92fc3f42b652492fab559bfc3303e3548d034d028ab72345926f2dcb277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d48012faf7647e67f60e11fe60ffcdd6d7497bc426017362904ed0c4742f892`

```dockerfile
```

-	Layers:
	-	`sha256:18630d03486907ac6ce27056c367bd6f86993647822285767883ab4216cb4f8c`  
		Last Modified: Tue, 18 Nov 2025 07:44:04 GMT  
		Size: 7.4 MB (7369997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45a7aac9b3d554e8f652a6a9390c16d41d36843cce4664f2eb431913946300c`  
		Last Modified: Tue, 18 Nov 2025 07:44:05 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
