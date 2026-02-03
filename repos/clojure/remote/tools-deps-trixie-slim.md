## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:a8ea831440d5d46e98d799d84866a155ec447b424fdceabe43ae87d636decfd3
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b18a28eb7f59441561bc70d8dd356a05b6efe27b3ffc3f138d1381e0475b1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193820767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac9c74fc22a0168cde3856a05d4547b1c631853685bfffdcc0c03bc287f5184`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:22 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b540b3318991f4e54a0471b3f77dce1c1123964264a53d0ae8209e7a2e6a9359`  
		Last Modified: Tue, 03 Feb 2026 03:24:00 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f58928dd350de9cfe22f0248a8ece55466cbb8a1aae759a56ab506f8f0a75c`  
		Last Modified: Tue, 03 Feb 2026 03:24:00 GMT  
		Size: 72.0 MB (71995828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad05bb0df7c12faa5d2ec1251b5f466c52331561769232d97cf9880eb7c401e`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3522889447b74cd2e29b06ece1f1b7c925e97a1f52a7dcb66e466b22838644ff`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf2b05e9ae7b6e204b1264e224eafbc1c1cb4219b674ae3341d66531ebf5fb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb321fe2eab2a9bc2cca65d485710d1e7bd28b169b3f4138ab9d89da672dfbe6`

```dockerfile
```

-	Layers:
	-	`sha256:8891dc6aa94e3962eabfac3eb26e2cf9603e1ff2b6e1ec978a651bcaf3a5865c`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 5.2 MB (5207649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c116ef852da9dbc466d6ea0b95028869391302f7db737c12628d89eaac9983ce`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72387029d63fa5b36c97d4ec88f27ff7cea5fb26bd21d11f7a29f804be7543da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193000202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7318a5825062b68d69968a01afb6402281fe928678950ddfaafcad21d5e759`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:25:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:26:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:26:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:26:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:26:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:26:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9933a2c1c0a153814ddb64b556f62b410322f37479af4eb2a4d1735bf4b2099f`  
		Last Modified: Tue, 03 Feb 2026 03:26:23 GMT  
		Size: 91.1 MB (91052508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612850548fa3d50fc0aa0bf71812cf029232fbf0805e226bad353f3871911d6c`  
		Last Modified: Tue, 03 Feb 2026 03:26:23 GMT  
		Size: 71.8 MB (71806588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fcef2967b8a40c9b5ceb055f024bb74ac9dbaa8c262ef1ca0bc86fa6658943`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4683204efab797549e4aa087466c7fdc841a33f17a8894f8cb20182b741b0852`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60610c42a182f0fdfad0539dc199857404d8192d14c97ea4db2f916e1dc3480d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abec546f3c3bf87a48e3150a1224f8fb6e02eeda804560a2c42a6ef2f8a53b2`

```dockerfile
```

-	Layers:
	-	`sha256:7689ae261da9e8ef8833d2610b10044a369b239fa5716589592ad50347820a8c`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 5.2 MB (5213439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2595255174e7c49a7dfa84dce7b324c7fb553608cd6a705037f4d7b640ee776`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:78771bced1fd66f4bb2422263bd4c18f30c118b9cceec7cac9b82c745648df65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205797960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a12761ab010bd964700baf980b9362a2d0d153ea16f7e2d489c139557146a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:35:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:35:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:35:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:35:19 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:35:19 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:36:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:36:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:36:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:36:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:36:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b367f49452386f5648bf3948a486b48474525977f8798c80af3b3240722b801`  
		Last Modified: Wed, 28 Jan 2026 18:36:52 GMT  
		Size: 91.6 MB (91610768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e49a8135c0c38402a68bed3899f1be03cf9daa420180e6f02d8d762067deed`  
		Last Modified: Wed, 28 Jan 2026 18:36:52 GMT  
		Size: 80.6 MB (80590551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f24a09db3b09c303855f1919a89d7aa5163b891cc73923e351d326e3ed9707`  
		Last Modified: Wed, 28 Jan 2026 18:36:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f362db66306491abe62f8af55d27fd05bb078a8acbdc99051e656ec7d92e63b`  
		Last Modified: Wed, 28 Jan 2026 18:36:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6ff817a276178b9d3681742c149218913d7d1501a177ddf6102f06b64d82790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51404253a1f9da8bcba507a236d4e06dc1f61ff629c9de297e2ce6bc9d3c2c2`

```dockerfile
```

-	Layers:
	-	`sha256:3daa0930804d38ab127e36aed5b991c78871188c7b99b7400add0df74a704cdb`  
		Last Modified: Wed, 28 Jan 2026 18:36:49 GMT  
		Size: 5.2 MB (5213330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5abc4fa8d173ab74d751997b4d8a48a10acd1c08f9ec4622ea605a2bc124f12`  
		Last Modified: Wed, 28 Jan 2026 18:36:48 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:92e2532348045ed47c435d3a11544968b274006e8f30e983c0c18b57a466d891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189904353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f35ef2374dbfa7a85fe46bcbcdd3b4b763aed7599dbbd585ca730f0b98c211c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 04:35:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 04:35:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 04:35:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 04:35:53 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 22 Jan 2026 04:35:54 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:57:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:57:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c69cdd71ef06850eefda28596d4212304f3101cd9d101f44fb4cf0c74701f3`  
		Last Modified: Thu, 22 Jan 2026 04:41:12 GMT  
		Size: 90.8 MB (90752894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6d3a24e9d95f0a53d69ef1e185241c625a41b38f404e11d840c904103e56ed`  
		Last Modified: Thu, 22 Jan 2026 05:01:36 GMT  
		Size: 70.9 MB (70878730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476d3e9776c236b085a0fac9bf9688b2075c785db6db5441d6b35b870153e4c`  
		Last Modified: Thu, 22 Jan 2026 05:01:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebf67b75368031bcbccfb2b55210c9b55d09be236a21b0cedd77ccbce8ccf1b`  
		Last Modified: Thu, 22 Jan 2026 05:01:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:19773bcbf4ba7724e951b0f2f421e37b20ebcdea7d8d22106a3925f36e843024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfa817792c85cf3a17a950e8e4baa05425bad4984aa40fd36b83fd7cd6ef340`

```dockerfile
```

-	Layers:
	-	`sha256:f836df0b753bc98eabb8debb449f1f6961b29a1334ffef48afa9a5bab6ef03aa`  
		Last Modified: Thu, 22 Jan 2026 05:01:26 GMT  
		Size: 5.2 MB (5197120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3e34b5822126bcf79d703e0039a9de285c818f46702ab468c3a1bd699b2126`  
		Last Modified: Thu, 22 Jan 2026 05:01:24 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:132210771cc44be11dd446c0b4712297a1bbd908ecd557a74ad5e7f405b3a059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191002946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d93c2c0f5d7649712bc4706e27b69cde7d25261f7da25be165a55e08cc10cf4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:06:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:06:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:06:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:06:27 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:07:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:07:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:07:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:07:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:07:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635f4900007f98e7f67419952a5a5a7cfdb2468fd30b472fb66d39a7f43c9064`  
		Last Modified: Tue, 03 Feb 2026 05:07:05 GMT  
		Size: 88.2 MB (88210676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d30b209aae8bc669b0bd50434d6ee84ea84f787f6df05cae709c30d051049c`  
		Last Modified: Tue, 03 Feb 2026 05:08:02 GMT  
		Size: 73.0 MB (72953079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a486f37d7d2af469188912a9690b840325e5a0764d0c91de82781b4c20977006`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08de98eadaf4068385e2da17c6cf8ab68e9e0ad636cee4506ae93ea7a43a839`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aaf0a2e9a57c1ac7fb2b851e5af2b7902d634509e0587df63197591e016c26d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00691f834f99bc6a50af25c515ace731396993a6ddd728131355876b06633866`

```dockerfile
```

-	Layers:
	-	`sha256:225f2c7e702efdb02f2d5e367bbcd1eed2f526c05eb65bde9e53289653515e99`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 5.2 MB (5206121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b06be872398bfc61363656079194843ceeafa2a8f4f82b797bb58d6a96ac3f`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
