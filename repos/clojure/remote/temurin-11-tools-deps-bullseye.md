## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:637ff6a4460f044f8fcef52fd3223ee4f5e4ed54d50b4689952409e5192b83e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:215ec9cd27aa4191a4b8602031976266e0c8e07b5b8f7de1179d6590bb2c1c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268265532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19103bcbab3193d6c6138056d74f9f9ec01e32965ef0e05d20ae52fba8a5f7ce`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:19:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:20:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:20:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34603f669cbbb7a2ab9fdb5390a53819343c5254dfd185cffacb123793f0540`  
		Last Modified: Tue, 03 Feb 2026 03:20:23 GMT  
		Size: 145.0 MB (144966643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1211eaf848e224de74a54a8e76ba4b6c1c2368c6c5caa4e24a1ffb016f214`  
		Last Modified: Tue, 03 Feb 2026 03:20:22 GMT  
		Size: 69.5 MB (69541984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac4b12f040e12d8d9cf1652a24f905bc576699bc0dfbab57fe5c5a66facf40c`  
		Last Modified: Tue, 03 Feb 2026 03:20:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:07a89c6f8d2ba1086cf07d4e5ac278f3a75298eaa6cdc5e83702d0bd5b803afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b135fd1a50589a31f3313f5593538ef7ddbcc529a9d73913adc82b23d79df4ec`

```dockerfile
```

-	Layers:
	-	`sha256:4fe274766a6666d6a034a11967de051505055b1f8ba763c740a63f720320b5e5`  
		Last Modified: Tue, 03 Feb 2026 03:20:19 GMT  
		Size: 7.4 MB (7416607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be6f366e26081c56f494a268cfa0a9c44d1a2b03ecb538de621045e57c1dedf`  
		Last Modified: Tue, 03 Feb 2026 03:20:18 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8869817ca88145bef74eb387f0f8961b4d83373c45e2a74f7a0db5a051639601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263682307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ce4eee1a21af6ca5222ceb96e711c411002f1142d90d9173ffb927bdd7c709`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:11 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efeb1c24fff21784756b734f50157ffb83edaa589ba28d420516fe75b4f9237`  
		Last Modified: Tue, 03 Feb 2026 03:22:48 GMT  
		Size: 141.7 MB (141729869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a089467b831e4f6abb21d7d241c26fe4f28f9a2cd3f0bcb5cc449b3ed19c9`  
		Last Modified: Tue, 03 Feb 2026 03:22:47 GMT  
		Size: 69.7 MB (69693470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e0d617f5a7d1e5a5c4275684b51472dab9e8f43de934d3b1d706874d4d47cd`  
		Last Modified: Tue, 03 Feb 2026 03:22:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ced53dd9e7eb49d46a0c576b018e72db9c4eac8cd798839e24de184b69588d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817a5d6504912115b6b9fe8b2c9d36f449dd0f4deb36fcd09c6620e86c4fa71f`

```dockerfile
```

-	Layers:
	-	`sha256:1692e0a6d865309fd4febc20761535d05f1607617873da32f2ab44a7afdfb3f3`  
		Last Modified: Tue, 03 Feb 2026 03:22:44 GMT  
		Size: 7.4 MB (7422324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3fe9c6d2ec7c2cad4e85595ef6cc8c42fa6cdffda289e760faa1041e30602c8`  
		Last Modified: Tue, 03 Feb 2026 03:22:44 GMT  
		Size: 14.3 KB (14326 bytes)  
		MIME: application/vnd.in-toto+json
