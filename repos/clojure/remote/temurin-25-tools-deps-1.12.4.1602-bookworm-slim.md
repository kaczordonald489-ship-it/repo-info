## `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:003ad307a57513165812804c4c3c5c9e1242902821da8281b433d0940384fdcf
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

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:96c796c5c6d9e4a03d06cb210a3985696bf8e02493a040c74fbed9e35367a0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189952466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63d972099072a59e8065e4ea22f5b813e6a13469c98c5fce9bdd0ec1fe144eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e604d36698b49d6ffdfc4ebf6b472e4b72903838c45ed8b8ce2125ac77b078db`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93a4d18e5e1dea61094a4cbd61a05b9e842844f0116db24a930e384a54165e`  
		Last Modified: Tue, 03 Feb 2026 03:23:19 GMT  
		Size: 69.7 MB (69677618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d84fe4618edc64552d4d0f130d8637a1b1d5a175ca8ec121ef96c8eedecde7`  
		Last Modified: Tue, 03 Feb 2026 03:23:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac9ea796828ed4e9799c5e76ef78d6c2027fbeae1a71363d9f6c63810a756df`  
		Last Modified: Tue, 03 Feb 2026 03:23:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:730942abac742df71b5d1ba921ec489223bd633f987dbef3a470a84c7379ffe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0717791d79936005b26bf755f184344408ec698622506efcd434fd0e70e1471e`

```dockerfile
```

-	Layers:
	-	`sha256:2becdf3b76fb46b254225327a10ec8997e78aa9bfa6dbf4e7f5fa6be07b5e1d9`  
		Last Modified: Tue, 03 Feb 2026 03:23:17 GMT  
		Size: 5.1 MB (5064760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6eb843f73793628a8125cc029961f17136383dcb7dd6ac12980b03da51568bb`  
		Last Modified: Tue, 03 Feb 2026 03:23:16 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e83490c5190ca8c02459b6c2f1aa0755687cae518aa494de07086f05f04df46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188834027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3ea3385d75ed5a854a9bc50736f1bd26e96e67acaeed9cc58d0d71b857382a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:22 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:25:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:25:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931c59504398c20167c6ffe4e72fc0de4bfb86bd123e49d19879505ab4f0ceda`  
		Last Modified: Tue, 03 Feb 2026 03:25:58 GMT  
		Size: 91.1 MB (91052493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41bb0c79f3cc36967fec5e06991d5dd3d94b3f1e4f939efec3a8ec613000e20`  
		Last Modified: Tue, 03 Feb 2026 03:26:03 GMT  
		Size: 69.7 MB (69672668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7baf818978427067c91e1d80512e1dbc48a8969524d87f7d306f9a7e0bf862`  
		Last Modified: Tue, 03 Feb 2026 03:25:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75097eb75275d895fe5a9d72125fbac52a9e29c3b93f21f5091f055846bdbf7b`  
		Last Modified: Tue, 03 Feb 2026 03:25:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14aff35b91f33f4b634640edc1bf7bc1f964c4e43fdba539b53748d264d4ee2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436b29bf93de020c50fe8eee036a8ad61e1800e188301e9dd4f978978d69da73`

```dockerfile
```

-	Layers:
	-	`sha256:e7ff9fc002b487bea15602ee927376ad405ac6380fb303b26db3548c5188032d`  
		Last Modified: Tue, 03 Feb 2026 03:25:55 GMT  
		Size: 5.1 MB (5070542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d952f0aa028d70a1f3ee36df161af552a3552bed6a119172ba0a82474931a482`  
		Last Modified: Tue, 03 Feb 2026 03:25:55 GMT  
		Size: 16.7 KB (16665 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:64c207de6398be5f3e2c0f48d8b41e456ba33806402983f3541a5479dee8afd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199194417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb848e8e4e20c776f6a87fcc671bf84b1d343deea8ce6f5dc93c2c31114aab3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:33:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:33:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:33:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:33:14 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:33:14 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:33:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:33:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:33:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:33:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:33:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695e67ec4365d5667a0e97958627f135a74eac3bc30c81b25afca216532ec55e`  
		Last Modified: Wed, 28 Jan 2026 18:34:33 GMT  
		Size: 91.6 MB (91610768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4f1a5bbbb43fb0e87be14a08923f519b1e4809a3758a5b13693e7ff16b0222`  
		Last Modified: Wed, 28 Jan 2026 18:34:32 GMT  
		Size: 75.5 MB (75513899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cdf1ddbda4c0198fb2be95a44ee4ff3569f0a2452551c135bb236e4160564e`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68f3c55cd35269a833cbb40b657da990bfc7c829e846b2cf9b537ffbfc11def`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15010c3ff1def74c0d5bac9199e16424d875b6daf77b701fe9bf386e5b5bd069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d847de5d2756dee64046cc5b3683e43de1a1765f04656474a3e09394d52451`

```dockerfile
```

-	Layers:
	-	`sha256:04bf7b8ee92ef64fa68ef961787732a0df8c4da3c6ece755baed2238ad8f0bf0`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 5.1 MB (5071228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82527e1d078ef8873182ddd2a18c8104b3163e466f0e749afd0790e4d8c4a711`  
		Last Modified: Wed, 28 Jan 2026 18:34:29 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a6250c48fe8c49f03af1d2651e8731eb48f01ecdd3c1c95b36c3bd603fae1202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183585775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357a7c636a14700656f47d7e47d02e365bd451ec4b090bba1d2e95690765f2e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:05:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:05:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:05:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:05:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:05:57 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:07:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:07:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:07:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:07:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:07:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f3e464ac1afdd462f5598a495c02f0389af1076ca73c693f7f6ddf988c814`  
		Last Modified: Tue, 03 Feb 2026 05:06:32 GMT  
		Size: 88.2 MB (88210676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad8cdf8ee9a196dfdaeb5aa62358174048f38e8ec7bc7c32e768d3083fc4abb`  
		Last Modified: Tue, 03 Feb 2026 05:07:25 GMT  
		Size: 68.5 MB (68489674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cc64594205bff541ea8b30b4d7aaa63260cf16ba1eecfe2a3f1fcbddbe82cf`  
		Last Modified: Tue, 03 Feb 2026 05:07:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e29776bed472b7cc9fa7ee458ffcd87e648a03564837e0f022885c72cb2103`  
		Last Modified: Tue, 03 Feb 2026 05:07:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2920223bd37c9347edaee2636da1e71e6a06fcbd5667becb7aa68533fc24bfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704309642b4c7c30d3cb7f9895af9683911d8fb42f78b80c2361d92860b26025`

```dockerfile
```

-	Layers:
	-	`sha256:f229d8213eaaf733e24f2d842fc483171b25ca1d2a660cfc5de4059efbf88038`  
		Last Modified: Tue, 03 Feb 2026 05:07:24 GMT  
		Size: 5.1 MB (5058629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02dd942eda85b55f307df03dddc40426c01e701ffeb58ee03f87e2e6c7ac49ae`  
		Last Modified: Tue, 03 Feb 2026 05:07:24 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
