## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:03497efdeb61880a02f41a29b94b085ab9fd1c4e838374973857076a587e3c7b
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fa5372a9afcf01e70515748e438069a9857e8cc43808c0d9ceaf91a806adb14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242755121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a02c55234a1a7a712cd22776c7e2eeeb1c3a2a9e8a910cb398770b0392ab260`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:50 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f295d07c7c5d0e2654dfe82db92165757b50b06a6a5c4c1ff0234d83716795a0`  
		Last Modified: Tue, 03 Feb 2026 03:21:26 GMT  
		Size: 144.8 MB (144847973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bb8429bc0fd4ea103805b6ffa1f621bd72b1b40adf16df5c27a9c69ead8df9`  
		Last Modified: Tue, 03 Feb 2026 03:21:24 GMT  
		Size: 69.7 MB (69677619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fe8ccfc9fd5056296e128eef7c051110ede921fb0f7a70f5edf49a13e0ba87`  
		Last Modified: Tue, 03 Feb 2026 03:21:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa602ae0bdc9c11241f31cb8996058e5e5fbb5a8a8eb9c4eea7f38c794d7a3`  
		Last Modified: Tue, 03 Feb 2026 03:21:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dec56664046c7f74ea01d0181f07e3ac3a27cb37b6d47eef656e34270e38aabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f0c19550d5436b2100193a903b40d866a7b607ab43d550e313b1019f51bd63`

```dockerfile
```

-	Layers:
	-	`sha256:66baa8ec7c2852c0512a0a812e6b6712f26d3b219ce8a1b8d23828f49fa741ef`  
		Last Modified: Tue, 03 Feb 2026 03:21:22 GMT  
		Size: 5.1 MB (5113402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c26fb562f788c4e6f6aa0a2da1ac0ca1d58030c5647845fda16bb06475357`  
		Last Modified: Tue, 03 Feb 2026 03:21:21 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b2b24f6cfe0c761d2329bf90ccc529a84497b2aa63b14c6bc7fba2b2afd323b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241461385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf42ebba1cc380526cfb5b25dbc2827d86af5ad9b8ca0e32145da1fb91985d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:23:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:17 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87f921415b70c5defb89b48ff1907d3de16ce49b752ead2cb5aed4aae05dfd`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 143.7 MB (143679941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66485d8038d6c59bc275404ac4fd151a19208c394e609bc3bead681755a4c0`  
		Last Modified: Tue, 03 Feb 2026 03:23:55 GMT  
		Size: 69.7 MB (69672580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678734f73628b9fafb1d8b7a1771164ad0ea0f2ab87e7e9042859a9ab777c04`  
		Last Modified: Tue, 03 Feb 2026 03:23:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd2bd7e90d8e723298182831e55b24974a9cf897cbf79a2be565dfa233b284`  
		Last Modified: Tue, 03 Feb 2026 03:23:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3cc38c3218c268b4900c7a52215563b09abec701e645a1537672899e90bf4c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bd1e717bcf1bce771ca9dc1bfc4fcaa63686abe5f74c5ba86147c3ad70f687`

```dockerfile
```

-	Layers:
	-	`sha256:b3ae574678a3a31aab0e6cffbaec636c5d7b456c4beebb93e26bfb7da79d7dd5`  
		Last Modified: Tue, 03 Feb 2026 03:23:52 GMT  
		Size: 5.1 MB (5119163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af307791dfae616430ec9ae5534de5fca86b7a21934014b1dc0ca986725a187`  
		Last Modified: Tue, 03 Feb 2026 03:23:52 GMT  
		Size: 16.0 KB (15952 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d79810c9dd08716e2d466088d3a6c95f2f14be399e21ff5bf8c20f020220d366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252108454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a17618f318b991875309a1448d6cf2a183fc99b8d9fe3188de3250253c541e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:23:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:23:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:23:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:23:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:23:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:23:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:23:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:23:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:23:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:23:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2235c724473658ab8b44f8727ae7cc58c2e9f4d98756ff0ccd8703501e42f498`  
		Last Modified: Wed, 28 Jan 2026 18:24:33 GMT  
		Size: 144.5 MB (144524725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a8e4bcf1f532479fe5324cf0f32878ca76c90a1b3dcf2c3078fbc8e1ff7a2`  
		Last Modified: Wed, 28 Jan 2026 18:24:29 GMT  
		Size: 75.5 MB (75513981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98697a8313e90de9363e8094c714ca833538c42e0f87c751e7a7b52b91e10db5`  
		Last Modified: Wed, 28 Jan 2026 18:24:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ed640ff49ecfab009036a763a4360443dfaaaba06f8101fe437a05d025e438`  
		Last Modified: Wed, 28 Jan 2026 18:24:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8728042d3c8ee56020a604b741c59d33e4088fb962e877803abdb1e2ab23812d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577eae15a27ba8c1423a650f05452e25002d3fdcf9a552a8e9577da0d6b2c0dd`

```dockerfile
```

-	Layers:
	-	`sha256:e0dd961e7f80e8e60c7ba44e3f456cf7c869f59af799373b91123f5c7b30488d`  
		Last Modified: Wed, 28 Jan 2026 18:24:26 GMT  
		Size: 5.1 MB (5118560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b37222b05abb620dc3159ff832cdc3ef40eb04defee0ec97e58ee7bba586a0a`  
		Last Modified: Wed, 28 Jan 2026 18:24:25 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cd593b8f2050bd6accaad572bd8b48bbeb5a39f1e45cc0e5e981cc554e0c387c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230235103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48cf3f371a75ac8fc32a2331ace827ac978a8e5c017335ae9aac7e3151992e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:02:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:02:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:02:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:02:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:02:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:02:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:02:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:02:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:02:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:02:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf9f6639db4985d1e84e8038c4b90494dccdf796f555e6f460cf675ea883eb1`  
		Last Modified: Tue, 03 Feb 2026 05:03:27 GMT  
		Size: 134.9 MB (134859768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81c9c8d959066c2d48e232551ad21148b8d38df9a8a7c83ebe93d6dd85deb95`  
		Last Modified: Tue, 03 Feb 2026 05:03:26 GMT  
		Size: 68.5 MB (68489909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d63baec620b4d2ec93f2978d90d8aebb4be183bf5b921b62d0aef8ee03891e`  
		Last Modified: Tue, 03 Feb 2026 05:03:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ba913548e3e99ba3041255523f1336707d709f54213069c3e26909d7bc02cb`  
		Last Modified: Tue, 03 Feb 2026 05:03:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd9c3f556b1a37a0129314aabaa27157b41c8c29be594682bf8d714a3e2ba48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39807e8aa84a2e973cf8f232aeff6fb666e0a5eeaf450d895f7e12c8167d40e`

```dockerfile
```

-	Layers:
	-	`sha256:2c72d0f9ef7d1d5002938e03055cb0376d964cc61ae8f31af0694e020b94a675`  
		Last Modified: Tue, 03 Feb 2026 05:03:24 GMT  
		Size: 5.1 MB (5104723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51eace8cff0c8124b42438e201ee181f6c417ba634dbb8f1b6341ace644925f5`  
		Last Modified: Tue, 03 Feb 2026 05:03:24 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
