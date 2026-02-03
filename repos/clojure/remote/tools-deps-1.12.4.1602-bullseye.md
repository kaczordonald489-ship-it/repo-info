## `clojure:tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:4df6bb485001b876b8978492648471f8a1f96c1489202009c860cbdc63a8cd51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a19ea474e1f8937c6c20a241a0c6a43e41903b1a6119aa7fd3907fbe67f6b63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215344339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba75c17b647be20b843dca4e7a190542d327aa5f2e3bd0b1ba3028f7958acfb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb35b305ff7c52dcb63e19672dd2bda3fdda23b2462d7b2db5c5992008247b6`  
		Last Modified: Tue, 03 Feb 2026 03:23:19 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1672eae01b34f9db5a14490b460c5364bea894965c2f04ec86d4f7f3fb3e681d`  
		Last Modified: Tue, 03 Feb 2026 03:23:19 GMT  
		Size: 69.5 MB (69541725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94936744e59ebc4ddbaad2a79a46b921f6eca0e01c0f608c8be716d5de43abb`  
		Last Modified: Tue, 03 Feb 2026 03:23:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcf7e0c5f9d8c93b0689838c8f0da12818dc2002c921a665a812df0618d313a`  
		Last Modified: Tue, 03 Feb 2026 03:23:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28155660df16502b787977f9d26dab7153d19473a23d171477a653f858a814cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5938307d010680be9c195e5d75ccda6b8a83ef289642b9a94343f2004ed364e`

```dockerfile
```

-	Layers:
	-	`sha256:6c5618448d852e31ff09fd9f18ce8b5356c4d0b66324fa004b99fd82d1e735d8`  
		Last Modified: Tue, 03 Feb 2026 03:23:16 GMT  
		Size: 7.3 MB (7347806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62204fa02486223dee94e0c3c1bebb14d05b9158ac04ed90a272816e28a8afd2`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0f589801038254c6b03dfcee3577d4095ae17f1f93429a603744066fcb9c4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213005184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ecf73bbcb9b1f6ef64476399c0ca7d152f9f7e2e920e7484fdaf96c43bfb2dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:25:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:33 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:25:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:25:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c354b5a0698de916710f46faff8abab7eb383c6211534c209b4ad54bf593576`  
		Last Modified: Tue, 03 Feb 2026 03:26:09 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2f4b0615df0b745ab53aa8331af2eefee5691fc1b2deed5dbea02ef7c5753`  
		Last Modified: Tue, 03 Feb 2026 03:26:09 GMT  
		Size: 69.7 MB (69693338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31311247bb3c4b6f3c9c0f3ad9665e2d2e62b52bd649a8dab5d6867289315f12`  
		Last Modified: Tue, 03 Feb 2026 03:26:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be418adf736527fa4d44d0862e07ceca2dd87f8532d208373bcd35a63c44eab7`  
		Last Modified: Tue, 03 Feb 2026 03:26:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:42197711d145909546df8610a0afab786f9c726d937843fc32b02da3353581ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601caca3ea994e1425c9539e5dc114126351ff11873c213342e27d1d0a1bd58b`

```dockerfile
```

-	Layers:
	-	`sha256:c9796b0230604bc2df8de3b8bdfdb0b9779fbc12d6bd360829370d584fe625fd`  
		Last Modified: Tue, 03 Feb 2026 03:26:06 GMT  
		Size: 7.4 MB (7352926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba789740db30945b0ed5681ba7eb6f8849f7a2dd6bbfd080e2a5e4e7baf63e1`  
		Last Modified: Tue, 03 Feb 2026 03:26:06 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
