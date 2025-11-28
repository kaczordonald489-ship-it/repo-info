## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:65dde99a2105f15475880ecaf110a1ef7f71a140415f79b1cd261e4721249c83
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3bf54d1967ef44d8b1c081f003b2d13ceb1fddc9403fddb308207843d8933b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259599324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067b94543cf1a34c1a8952ba92514ca13cc04a254a78b185c1a935b3e5d5d1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:15:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:15:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:15:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:15:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:15:18 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:15:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:15:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:15:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:15:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:15:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db32e0627e4b925784a378b851cd03db60c66a7c2630ef435a4ebe00ee512e67`  
		Last Modified: Tue, 18 Nov 2025 11:31:21 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b4519f0721a23ca96d65cebb04d73ca313b79d928ebae16007c19b871bb6f`  
		Last Modified: Tue, 18 Nov 2025 06:16:11 GMT  
		Size: 72.0 MB (71995820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a673ea753251a5603f668b72c53b17a27aaa73087445b0308dd1808195d3ba1`  
		Last Modified: Tue, 18 Nov 2025 06:16:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02d756ea936ce1dff6dfff8f250a2d5510335b416181677f6792eb1bd79bc6`  
		Last Modified: Tue, 18 Nov 2025 06:16:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44e6a57e316040dc8933f1450dd88b8487e00901cf3064d4a46e0d728eb75024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493800e784422349c33a96377ed87f8f4935933df32bcde756d581fb28d906e2`

```dockerfile
```

-	Layers:
	-	`sha256:9e29fb6e9c034aed0e87d4a0adf078af8d0801c131b0ec8a70cdc68133d45968`  
		Last Modified: Tue, 18 Nov 2025 07:46:27 GMT  
		Size: 5.3 MB (5259301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b276ea616957200e4039f747c4b29f73fc6c518059cc00b42879590420090bac`  
		Last Modified: Tue, 18 Nov 2025 07:46:28 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ab43fcf5e41d3e03a6b5d2a9ed4ad1e657531b044d5299568e63b95204ff010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258055106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f7233572296680183e39784d1e03a6f566324f5638e7d2554d9145815050f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:11:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:11:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:11:14 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:11:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:11:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:11:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:11:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:11:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a712bb6f669ab6f8bfd51eaa5e7f94a6fa38cde19ba2c173bbc717b06bb82bd`  
		Last Modified: Wed, 19 Nov 2025 22:09:36 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80a3e29f071bbe209bd534ad036c9af6748df3539dd4817896a35d57df25858`  
		Last Modified: Tue, 18 Nov 2025 05:12:06 GMT  
		Size: 71.8 MB (71807873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea8ba032f9c269f6c31f75cf259b4113ec5eae61d4fbdd682c157d336c7c1df`  
		Last Modified: Tue, 18 Nov 2025 05:12:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599851cc4280f51255d6d361f8204c3370d992cad3339946828ce07a0396c65`  
		Last Modified: Tue, 18 Nov 2025 05:12:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6acbfb66c37dea157803df42b543635a790f2fab9eff92f0c7d41b1fc5824dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dc8330b2d213e7210a37bf64984d5298a504fcc5d6f1c05455cfd327560db8`

```dockerfile
```

-	Layers:
	-	`sha256:d83d18973f60e9409251cf321e687312f50563c41be260cf890c793c8af57b1f`  
		Last Modified: Tue, 18 Nov 2025 07:46:32 GMT  
		Size: 5.3 MB (5265070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8172f1438dd119b3998fed318cfc45b8cca2cc66aa56d4e9c10fa86815c13917`  
		Last Modified: Tue, 18 Nov 2025 07:46:33 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fb3dedda6ca46222036d893585160dfa1afed460b539411306199adda8fb998e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268932244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9c2daedd261029ea9a3fc66a41921c124bcffa92191e79494cfcf9d0556c46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:20:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:20:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:20:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:20:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Wed, 19 Nov 2025 01:20:18 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:21:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Nov 2025 01:21:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Nov 2025 01:21:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Nov 2025 01:21:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Nov 2025 01:21:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd130f2e8b75792a89896873c54ba2093ec400e1aa0bd5b59bd010122b0df27`  
		Last Modified: Wed, 19 Nov 2025 01:21:54 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5254b517921867eff35cafc61f5bcf651beffccca61dd528687d3bbbb9024443`  
		Last Modified: Wed, 19 Nov 2025 01:22:09 GMT  
		Size: 77.4 MB (77391408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6e066eca060e90b3d4c4be70e9aa09ca57248b7dce7986a61fcff2139276b7`  
		Last Modified: Wed, 19 Nov 2025 01:22:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bdcb8f167e0ec80b63fb6950166805b57ed0f6189f662793ec989bc6274749`  
		Last Modified: Wed, 19 Nov 2025 01:22:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3efa7ac4e1b0db9ba4bad593897bc6b81e7fbc4f0d134d21befe8c03fdbc5eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8882664dcadc20fea2e2571c625f977e0fd667f65bcb2f6713eb84bae4e32a2`

```dockerfile
```

-	Layers:
	-	`sha256:e88ecb0d3100ae4f3a2a7c02ae5bbd0a75c8ffa6c206bcc08ed7b644ac0d47ed`  
		Last Modified: Wed, 19 Nov 2025 04:36:37 GMT  
		Size: 5.3 MB (5263672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d21adcdb04c96c1575f99acfa20c7adab14adae0dadcf980678270477820a19`  
		Last Modified: Wed, 19 Nov 2025 04:36:38 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:ed8c33c48120465ac77ccd2ea4c74ebc0dfa70b333f31a6946f32a904ca7cdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256348991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff130125c8828d429c506c8a3eee9e11c95fc856ec9c51b3195b40325fe5989`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:27:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:27:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:27:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 18:27:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:43:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:43:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:43:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:43:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:43:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516f07972228dcbc55c70b87824ef60b8072c90f8a8787a93b8e4054d62735df`  
		Last Modified: Thu, 20 Nov 2025 18:32:59 GMT  
		Size: 157.2 MB (157194320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01afe0e6f99f498246c4bf39f4339fa16957e9fd851cd63ef2c95b93b254ac6`  
		Last Modified: Thu, 20 Nov 2025 18:47:48 GMT  
		Size: 70.9 MB (70880504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d5648f503859cd3ff3658f8fc69adb73868fb84beaae7fdb205ac32f59eb7`  
		Last Modified: Thu, 20 Nov 2025 18:47:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc3659a9d5a68ffb91a8e9b1f902404f839b2eb82b8e4eb29c5c70a8d1d6ae6`  
		Last Modified: Thu, 20 Nov 2025 18:47:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33b783f8928005e18eadf143c3f7db0270e1d13ffdd979ac1934682909c95b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed760e517e8b5a13be723cd282af13e8a2f438a56aec4d1bec71c9cbfb5d171`

```dockerfile
```

-	Layers:
	-	`sha256:f4cf391357ec690ce00b6d71dd029c8128c9dfe9c17b253311e3bbc60ff43124`  
		Last Modified: Thu, 20 Nov 2025 19:37:28 GMT  
		Size: 5.2 MB (5248765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25035b68b126b2e1b4a2f81116f1c8889bbc153fcb95fab217f3ec5842ca4471`  
		Last Modified: Thu, 20 Nov 2025 19:37:29 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2e1af57fab380ffa569e00454c4a15dc87145a2386a0fca8fc57e12680e26f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249858791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5add7c789c919e7d8a701d87b15ea2e842390ce1731fa6e87226410385f1238d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:29:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:29:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:29:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:29:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:29:25 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:31:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:31:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:31:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:31:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:31:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15456efc8c56111be75fbb32203283de9917eff33d36ac2a49eec5455d7ae626`  
		Last Modified: Tue, 18 Nov 2025 05:30:10 GMT  
		Size: 147.1 MB (147069840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6983a416f551b134a61f7c3123e1680f003856cef2bd8e0384e804b81e91c`  
		Last Modified: Tue, 18 Nov 2025 05:32:03 GMT  
		Size: 73.0 MB (72953539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a388cec002be3f4a6bd2c71215f8e19f0e6035e83213099a8cb4afd9aad3fe`  
		Last Modified: Tue, 18 Nov 2025 05:31:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef51291c7fbac66764873c939c54008438e085b1b2b7cae0b1267f21a20d683`  
		Last Modified: Tue, 18 Nov 2025 05:31:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b83bac9bbe9a68f0787dabcfcafe980bc2c21af939054f73157504b3b3d4d852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598d1dafcb4b5666cca15463e3c0edbdbd88dae8f84f174153f3b36eb0cd6b4c`

```dockerfile
```

-	Layers:
	-	`sha256:be62e75e2b27c4bf500cbe561f44329ee7523163b5c3c1f0aa00fffe1191a48c`  
		Last Modified: Tue, 18 Nov 2025 07:46:45 GMT  
		Size: 5.3 MB (5255225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b46d73704b6d96e43281e142543785f523aa5ff1bc10b879c0f865246aef07`  
		Last Modified: Tue, 18 Nov 2025 07:46:46 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
