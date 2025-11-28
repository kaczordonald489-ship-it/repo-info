## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:49a296d58b2d673150537e9f611ea4956c88f4d80850eeb768e30d55da771e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:805c7b108e6ef3d855e8ca31dc0f589687fc9065f429c1c83568cdc45d46619f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189564866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdc421efac734cf02c83b7863562fc986004281c96d080b238d2b68e583cd18`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:16 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:05:16 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:06:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:06:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:06:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25699c93dc7bbeb34f328faa846ea6e7aaebd3e2103f6a7415ab228753165c`  
		Last Modified: Tue, 18 Nov 2025 06:06:00 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb51414ba78d81977edde665aab5ea3df9948185f3b0f92627dd53acb7d19b`  
		Last Modified: Tue, 18 Nov 2025 06:06:56 GMT  
		Size: 85.5 MB (85541285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa98989f385b508931e4268476af7cd7b2e44d7ad051c4cdb3355ada5500ca0`  
		Last Modified: Tue, 18 Nov 2025 06:06:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:05fcc8009580ce3c15e5ad27e2295b73ed86346449e9236d52cafe94459bda9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ce9882f5fbcf29891a682541c0113dce889847a4c22d4b3c4c610b7e82b12d`

```dockerfile
```

-	Layers:
	-	`sha256:68eecc62022b065f87d6ae9a1b873e1f79df78e093b329898cea1f74b43504de`  
		Last Modified: Tue, 18 Nov 2025 07:51:20 GMT  
		Size: 7.6 MB (7588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b640f335b5f7add7c824c48993efa4a4e5c0806ef5d34c9102ac0847e7c6ac58`  
		Last Modified: Tue, 18 Nov 2025 07:51:21 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56b9365f6f2da6cda0122716b4488b36f8f101a06f8b992edf570a8fbb4060cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188830580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56655f7a06d928ac59701b54a81a960bc5251643c015cd5e7dffda09fdf91da0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:54:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:54:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:54:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:54:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:54:55 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:55:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:55:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:55:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d390101a8f55dd574426378320adc57b317b7d2c43dd7873fdc952d32c4bbc0f`  
		Last Modified: Tue, 18 Nov 2025 04:55:45 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6720f81e97a3fc85826592062d73cff1f275218ce9eb9aeb139d43cb1723f95a`  
		Last Modified: Tue, 18 Nov 2025 04:55:44 GMT  
		Size: 85.4 MB (85364704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c1d0ee4857da2b139e07757eb24f7cdadd235c863cea189f177d2555af987`  
		Last Modified: Tue, 18 Nov 2025 04:55:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c3754f9d7015ef3414290ecfef8efabc7705dc7bb0ba37ba0af12f1aa507ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcef8991e2419189d5ee1785f3915d89dafd522b211cdbdcfe645e104a4c21`

```dockerfile
```

-	Layers:
	-	`sha256:215f12de1f83ae166bcbeb2ac3d014c4dbdfc98d0b59c19b3ef140e1ff76c170`  
		Last Modified: Tue, 18 Nov 2025 07:51:29 GMT  
		Size: 7.6 MB (7596267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f485552a7dee6d3cb9bfdd141fe06b8dee9af69739515b815e1e8a1f6a5e47a1`  
		Last Modified: Tue, 18 Nov 2025 07:51:29 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a2ba56fb4fd8e19343cfea6045a6463df6b28195689143d79532facd52172695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196231678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724b27a32dfcf5c5ffa41a515d0139e84dd0d7089ae168a9f93a541dbe34a2a1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:14:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:14:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:14:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:14:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:14:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:19:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:19:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:19:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d016d9e912cb735827e82c51514523b6941a4ca5114f7db6b8ad862763e4a5`  
		Last Modified: Tue, 18 Nov 2025 06:15:45 GMT  
		Size: 52.2 MB (52175144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43f3cb5c1b0470995ad773b083f3862e73af939c2738d9e7e64dfca7cb8cf7a`  
		Last Modified: Tue, 18 Nov 2025 06:20:10 GMT  
		Size: 90.9 MB (90947406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404a6710fc8052aa06ba2008bd7c0505badf5e04b114a42f0310c1831688d82`  
		Last Modified: Tue, 18 Nov 2025 06:20:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fd5989580e51825eca83f97f1ba4029f6b8827f9437296bc85e1f3076cdd752d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f930edd1096cc5e3bf95a9e818e6e324982ba91546fa9c83f7401e12ed4421e1`

```dockerfile
```

-	Layers:
	-	`sha256:5bfc625f2ccaa778b315d10428db67f4da16c7dc90dbab74b00e94f7df1fc2a6`  
		Last Modified: Tue, 18 Nov 2025 07:51:36 GMT  
		Size: 7.6 MB (7593551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48714b7fc486752407aec95a093cb557fde9f500c838b2cf10f956217b8682c3`  
		Last Modified: Tue, 18 Nov 2025 07:51:36 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
