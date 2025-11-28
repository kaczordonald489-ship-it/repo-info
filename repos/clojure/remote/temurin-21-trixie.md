## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:02321200a34bd27e9f87a115c7b679522c71e5ed227ceda15af434ed267d33d0
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3cd8d19b468d9c5178d1013d970d907c6be4de187edc1e4934f73a2a4c3babe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292657812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a943ead0d7dc361d885b66acd32645470e88fd673dcef38f83f3dcacf190d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:15:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:15:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:15:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:15:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:15:02 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:15:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:15:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:15:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:15:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:15:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1dcd44f04d64f4839a00010453555601ac13de7b46484c3297b8a74547d4de`  
		Last Modified: Tue, 18 Nov 2025 07:51:05 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b76d979f559b6cfc66bc18fc2bffd03686e16aa7d972837c1859f13448ca9e`  
		Last Modified: Tue, 18 Nov 2025 06:16:03 GMT  
		Size: 85.5 MB (85541247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c775868c2a603bb7f7f79fa1094c1da84c44f9a0c70fab370a737d226bdce2b`  
		Last Modified: Tue, 18 Nov 2025 06:15:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6cfa8c279153bd3b858d5de6c973d61e9251bac4b1ed4ea02d05b78203c8ad`  
		Last Modified: Tue, 18 Nov 2025 06:15:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8976cf7419d02cc8fc34b8dec9c50dbdc223eaf36a980b043729d19394ef9ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2bd6160fd8082a3774d7de8de92355ae0998d993e36cd193eee54838d67292`

```dockerfile
```

-	Layers:
	-	`sha256:c829aaec05231372a0559a3c1c2f22707fad3c26ee20a6bbeb1b355d73c9b95a`  
		Last Modified: Tue, 18 Nov 2025 07:46:14 GMT  
		Size: 7.5 MB (7470033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a27c214e471ecb790a0a3e0c879c62b82e0e0c17ac92ce56e3ce89d5dfe69f`  
		Last Modified: Tue, 18 Nov 2025 07:46:15 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e924e32be166fb9bc4889d7a76c0dcd8df710899066fd76db12293596d17505c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291123776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3237d8e8ca9a9f93f2679cd9756f44476af8393b318d0fcd66880b9d06c2ff17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:11:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:11:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:11:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:11:02 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:11:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:11:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:11:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:11:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:11:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb85b785793fbeca8266a2cf928124f95b5a947ef0d44404e34a423377b8277d`  
		Last Modified: Tue, 18 Nov 2025 18:56:15 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ebcfb2c9296717840b76a73dbd912eb20a9c1d28ad6e5df74d9b1cf829544`  
		Last Modified: Tue, 18 Nov 2025 05:12:04 GMT  
		Size: 85.4 MB (85364862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af545bb22139227989ad2fb41523f3b717484131683c928237ad7e9f860590f`  
		Last Modified: Tue, 18 Nov 2025 05:11:54 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f09f2e3465cff412ace3c814706f1a65095f56799e0e000e32407baf8005f`  
		Last Modified: Tue, 18 Nov 2025 05:11:54 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8c4cbb74d4b3c1ab1996be7203acc050d50cfde649c18bf9938edc51e9d3514a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11577991528bb208fd0a1f631e437f4d06c91bedcdd520eae9d964512065c59a`

```dockerfile
```

-	Layers:
	-	`sha256:ae1dd1c32a761d839a126718a353a0ccbbb7a8781413dbfb5d47c262c65a29a8`  
		Last Modified: Tue, 18 Nov 2025 07:46:20 GMT  
		Size: 7.5 MB (7477063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acecf262de302f4ddf1b547c627cfa0e3f7727a89d3056c38eb804a6720eae27`  
		Last Modified: Tue, 18 Nov 2025 07:46:21 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bce8db0920d00e85f6c4a102eb68dbc4f86d64958f3ed809b8f0ffa2450cb638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301999727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ed7062e89dcc87f3edf0d8b78443d9c5350e5d9e6533901843f2464adf658a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:34:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:34:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:34:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:34:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:34:29 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:39:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:39:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:39:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:39:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:39:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c7f6d790536283fa4178bfde3ea5f1b1cc9108e82e0ddd4085ecfe61c31b5b`  
		Last Modified: Tue, 18 Nov 2025 06:36:19 GMT  
		Size: 157.9 MB (157942949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212dedacaca08110bb4ec361df558cc1ccbff428c9856357b3c6a0b12e4127e4`  
		Last Modified: Tue, 18 Nov 2025 06:40:50 GMT  
		Size: 90.9 MB (90947253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bc3311f64c7ff7f71865a5ca1314019680bb99f313b0fd48e3157b9436060b`  
		Last Modified: Tue, 18 Nov 2025 06:40:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37780bc7fa6c118fc9d23f0161b113ecff1bdd20cb20c5003ed993580c8ed8`  
		Last Modified: Tue, 18 Nov 2025 06:40:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:45dbe0b452a64a99d589b3011cdd825bc97380b4c3a66bdfe6992854f266a11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5e03d8404901b600d30744212f15ffe05ca96a4f96c0c61452ac60f3e5e80e`

```dockerfile
```

-	Layers:
	-	`sha256:98f63283aa8d19715cc61ae5c5f5a0f8947948caf9f2a32730609c05723fc811`  
		Last Modified: Tue, 18 Nov 2025 07:46:27 GMT  
		Size: 7.5 MB (7474452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80da644a2b54088276367fe57f73740db88386acef06723e0e69e53bf5b00a6e`  
		Last Modified: Tue, 18 Nov 2025 07:46:29 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:fe818d5cbf1f07d5689a07d8550187fef5f993bc18c8aaab33c528694acc5740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289392999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6022d64abdeca198fbff87174f36826d9e9b6714e1bc993288ecba9052bf4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:20:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:20:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:20:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:36:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:36:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:36:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:36:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:36:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9510e39712dd763e37991974565f84df07e5754bd9efcade332f8c04005a4403`  
		Last Modified: Thu, 20 Nov 2025 18:38:42 GMT  
		Size: 157.2 MB (157194242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a0579df77c747c2a8c3bc55bf9d5d4e13de4f00e9be47ba33d3534531a8e94`  
		Last Modified: Thu, 20 Nov 2025 18:40:49 GMT  
		Size: 84.4 MB (84426521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9f24b9b7df127d57f113d2a8d2e41763bd0a4211a05b4a6b0bf84c4d0e4f8f`  
		Last Modified: Thu, 20 Nov 2025 18:40:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97db8818b672928861d749f862df5a4771f2ccb89f472f5aee852c693633b4c5`  
		Last Modified: Thu, 20 Nov 2025 18:40:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f50c8d80d9c69e669c12c3da7a1ce5fd30d20732e2f03e6e41da7cca8d30276e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469dddb5fa20b43fec4f2b57e70dff7248743222ba3141f23cddecd8dcd4ef5d`

```dockerfile
```

-	Layers:
	-	`sha256:6bebe4a4131ba6e0e093cfeabec26b3f03c8046997570f2d9c534faa66aa824e`  
		Last Modified: Thu, 20 Nov 2025 19:37:27 GMT  
		Size: 7.5 MB (7457946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2929afb545f8eb7491aad0cb2ad0a46fe776f2e89075a88febc9d5b38fdf3b`  
		Last Modified: Thu, 20 Nov 2025 19:37:28 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a372b32a440cdb3a02a92da81a476eecd238da4df753cf853c5228c432baecb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282928053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041399c2c7606262ca6083d261ef6c7ab83b3d44d424f1f293a66f2955a88d81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:29:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:29:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:29:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:29:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:29:15 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:30:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:30:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:30:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:30:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:30:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8a57fefe2d70f30d604267be848d56002a7ea2490463d77ec5cf62b33d73df`  
		Last Modified: Tue, 18 Nov 2025 05:30:00 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97962cfd507b4ec3747250da059e9775df9c8a4a5415483a78d94c4cc74f6533`  
		Last Modified: Tue, 18 Nov 2025 05:31:29 GMT  
		Size: 86.5 MB (86511167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fa980ef39c146093edece1d0b620c90815251b073b641624f6d7b94a55286f`  
		Last Modified: Tue, 18 Nov 2025 05:31:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d0097184c34e48f766b0e61ccf5315f013e5fe873d1ebc056557022cce2e75`  
		Last Modified: Tue, 18 Nov 2025 05:31:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:855f26ae1ac5920605d657a1e8478940de58506c17b93cb62ef7ed01114bafaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4104f91229a862cb24c24a1c7934cce75a2eddbbc07e4c535f6dbb54ca3fc2`

```dockerfile
```

-	Layers:
	-	`sha256:b833f507f614de8b6a2cf10d14bf26b4a426ec4a697ea9e6614f6b837508aa42`  
		Last Modified: Tue, 18 Nov 2025 07:46:40 GMT  
		Size: 7.5 MB (7465955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc729b0dea09cbd736ae7034a4580c34594e07a9bf9625827dc000874f27d03`  
		Last Modified: Tue, 18 Nov 2025 07:46:41 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
