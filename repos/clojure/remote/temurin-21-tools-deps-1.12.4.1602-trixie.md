## `clojure:temurin-21-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:72053bbdffdddd0c48406e4a92ba98e78dd156a13d34cc7f9d71ff291d43e892
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

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e53e701c665af3ab6df2dee29a496c7b74860daeba532e0c0a8f371613549672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292662531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2761fcfd1eaad10eb55f30243a0b7d1220c42cfa56847aa5d9f387ea58e5f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:05 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f184b04661eb30804816a1f402aec6fdfdce123ce9bcc80ebf75c84c2f5bf3`  
		Last Modified: Tue, 03 Feb 2026 03:22:50 GMT  
		Size: 157.8 MB (157826000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d733b8fd63c4f045d3bcfa2f0924f527b5b19eddb8252a85911aa2e07a32edd`  
		Last Modified: Tue, 03 Feb 2026 03:22:50 GMT  
		Size: 85.5 MB (85542536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d82b1822740e6972da4bb63ed4b9f44e96b66bde4cd0b26dc59218c25ae438`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c708b8ae63bff14364e9919f12ea780401803a1eb4788929c0ded73d462c9cf`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b305876366aa4c122042bda33c1e6dd153d3cfcb155625e4d81071b6dc1ceb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bf9ceca861676a7f34afcd71c5aaf509dfc39c49b3e13f81969ae57bf83ceb`

```dockerfile
```

-	Layers:
	-	`sha256:60828d156e1473eb28fd82905747153ec14cbf4935941c0d6cacf2c102209e80`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 7.5 MB (7470930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950ba7e721b9d54860c8f52f99699db327589ef668cccf59eaf843dadf19c226`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c94a47711229a407a05df8977d4ec90f1692dc315d028db3c25e2aa1f5916dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291122185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5db1229c42c907ea49901e38896be839efc277d0cda5f128a362c72e44e6109`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:39 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b7bc9290d9582b559e900cb5895894bbde7f612b783b62074c45f6f3c30a77`  
		Last Modified: Tue, 03 Feb 2026 03:25:23 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ecd594bfa7d9a9ed39bfa5dbfcefc584d9a4b98d34d6f1c78c67842d33bd1e`  
		Last Modified: Tue, 03 Feb 2026 03:25:21 GMT  
		Size: 85.4 MB (85361544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb6670df4ce762076c68bf4855c33437193b44000108292557e67bfb468e07`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b391029a1f06c550adf155edc6cfdead5b2982930536bd12260d73ab2dada`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e0f3479629668b4feeedfbbdce59277c7ed8df575dc2a4282d576c3a076ef5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db944a94e74d558d09f4e2d1f8402c4a4ba74c0dbf9ad9936a5b748a8515d8fa`

```dockerfile
```

-	Layers:
	-	`sha256:667524a3c67a8ddf1c66fa964662e7824216f293f8e12c6882a50a3800ff3b2a`  
		Last Modified: Tue, 03 Feb 2026 03:25:19 GMT  
		Size: 7.5 MB (7477960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8089adb9b420306b1bb46e5d9a5ff65c6d953436c639f7a31c1c90f3030f9f4d`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9511ee590f3a2493b80463724217dfa5588357959f5ca99a51c93ab94e24959e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.2 MB (305203821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9f779f081b356f7e2d3e3ef7ff2cfca6e2683132d8fdb2626ffcc244ed0a28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:29:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:29:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:29:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:29:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:29:53 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:31:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:31:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:31:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:31:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:31:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea87e0e784dfe85d8229ea938fdb15a9cacdb83d0d027e8baaa0ecde041410f`  
		Last Modified: Wed, 28 Jan 2026 18:31:54 GMT  
		Size: 157.9 MB (157942993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d398edbc6fc721fa46395321fe65ef2a86da27b1128ac7edc6da0f0a5ef04e3d`  
		Last Modified: Wed, 28 Jan 2026 18:31:52 GMT  
		Size: 94.2 MB (94152822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585460290d270fd54ba69f7bd8c6c45c7974a6d812121d082365bd9dfc471aa`  
		Last Modified: Wed, 28 Jan 2026 18:31:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b18b5692e13a66de89c7f948d3e20ae6429dc06409366043ff7095b393808e`  
		Last Modified: Wed, 28 Jan 2026 18:31:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:94188ba1324cdbe9020b27a28c5d96d87ad7865fa67637dbe818a1854e46e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b63bc1c8585ad4170fd8a50c4aca2d4100560f1724d3dd8dea73afc31a321bb`

```dockerfile
```

-	Layers:
	-	`sha256:8552a76710d249d59250b667e966dff5752ff3474b2a4ea73df39728f52c92fe`  
		Last Modified: Wed, 28 Jan 2026 18:31:49 GMT  
		Size: 7.5 MB (7475351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15dfc3105b4243e751614a2b216618d1ed51f53909d03a9780cdb2df5d5ad38`  
		Last Modified: Wed, 28 Jan 2026 18:31:48 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:fe8ee9b51a8fba87ead65aed2a0b40bfbf9195a3e66c4d1d2e05dae5a6aca197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282936793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1c0ece527451e41d47f2ba46f81c99396ad58e1ab95001b3f7952b14f40fa2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:04:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:04:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:04:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:04:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:05:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:05:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:05:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:05:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:05:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110ef213ad849aef62022029533be2a09b2a6759b6635f693b2cbce0bee3834`  
		Last Modified: Tue, 03 Feb 2026 05:04:42 GMT  
		Size: 147.1 MB (147069858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9a556dee36c513fff680a331219bd24ca58ae13d457f952f63b84400410d8e`  
		Last Modified: Tue, 03 Feb 2026 05:05:43 GMT  
		Size: 86.5 MB (86511515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67c8cc894350ef361ae138d6162af685bcd328fda94520d811546b0428e9161`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8156331dd40d2df91e3630c0685968b6a25e66b56e71426bdee82f2f4b797eff`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:660d1adc1bca0705c870ae5df9c183c99159fda6f3362b43b5f7e206ba4c26ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b4da031ea53bdb9e6fd89d776ba76d17f9f6ca41303b65e4a06d3b57c2ed3d`

```dockerfile
```

-	Layers:
	-	`sha256:7c8beab1a95cd7165a7b4edb80543c2ae5c33acd3c3fe835bb392e99ff45b90a`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 7.5 MB (7466852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a777756a512adf1b9aa0f6e696b2e858dd43993749851d7d89d0806dbc937bd3`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
