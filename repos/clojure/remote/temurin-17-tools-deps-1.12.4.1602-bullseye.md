## `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:1d8428bca4fad66d23aef7670f0fb6c60df98c61e9b94c964db3409e3a024e2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b50fc50fd4ca702ba13dce637b4b0abd594ca8dad63919ea802e598859e39b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268147108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725f724696e7fa31874ff4989628446052654affaef157c8315676e6b005f37a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:20:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a12c87c3a7bc19fc13cd4cd5fa72449d9fb77b92cb79eaa447c14521de520b`  
		Last Modified: Tue, 03 Feb 2026 03:21:28 GMT  
		Size: 144.8 MB (144847923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47321c779ffbc4944652f535d00cdaaf3179da366959b6d327b3617d605eef5b`  
		Last Modified: Tue, 03 Feb 2026 03:21:25 GMT  
		Size: 69.5 MB (69541881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a859b925cf02e338933190a0570efc5fed88ecedae3b53a4de92aae05fd9ba`  
		Last Modified: Tue, 03 Feb 2026 03:21:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaaabcad38e299df7db7ca35a3c2783c2a72e5ad8a0cb45feb55951413a7f3c`  
		Last Modified: Tue, 03 Feb 2026 03:21:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c95109a53e56f0289a4bb22ffee4578daecb9176282a39188805164b1ae21ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a0ca2ab0ea454342d12f222ad20367077fea9a63723c97e2c197bb28eb4e24`

```dockerfile
```

-	Layers:
	-	`sha256:426494f57344194af00c8aa2c1665d468a29b4e76066b17bb70fa57dbac5e5dc`  
		Last Modified: Tue, 03 Feb 2026 03:21:21 GMT  
		Size: 7.4 MB (7396468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d162866ca85adf21285537949a203938241064b0d6e28c7219e2667e13f04705`  
		Last Modified: Tue, 03 Feb 2026 03:21:20 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2de9ce290b6b0225ff49913ac983835e55c1175b16c86bc7b518687b2108529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265632536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4516120d5962638c0cd4dfabfbb2cb373229c67e0ce980a2b809902bfdee8ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:23:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:18 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef30a6de8c751fdbe202680a9bd091c97f73efaf9f0ec5c27170036cc104a62`  
		Last Modified: Tue, 03 Feb 2026 03:23:55 GMT  
		Size: 143.7 MB (143679941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095eabcffe787f24121b7aaf3cb86038e74ac8ad598d108eac6995d495c7ad58`  
		Last Modified: Tue, 03 Feb 2026 03:23:53 GMT  
		Size: 69.7 MB (69693229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899b7faf33d45451e5da483d9e21d4558a5256102147f46dd1edf2b89dc8b8c5`  
		Last Modified: Tue, 03 Feb 2026 03:23:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1804a5c1f1a096f545480444d067cd9455a6c7329070e65a9e10e6d6e18ce1`  
		Last Modified: Tue, 03 Feb 2026 03:23:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3f63fc735bede243082318a3c5205d8baabc9d1cd05ce56d2019585975f79c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e540f33dcf672a6220473c1a66c36908c598cb5575b818812bdb7eb086b00986`

```dockerfile
```

-	Layers:
	-	`sha256:ecec9cad45c283a1706e3e5b49db0366cf27942426c8247a3f2a07b9a055ba90`  
		Last Modified: Tue, 03 Feb 2026 03:23:51 GMT  
		Size: 7.4 MB (7401567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:643cd8e3bf2c669c009403dc87f05cbc760c52a8b6fd44474af6b10b8e604bb7`  
		Last Modified: Tue, 03 Feb 2026 03:23:51 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
