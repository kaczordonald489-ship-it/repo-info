## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:ecab0b838ca67af132bc4a3d5ae960e6e0a502d20fb1894d251006e31d0620eb
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dc7fed0b17ede7a18bebd22e9d7676d4b77290594019895ee142c31ce08b50be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274599167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae67358d44b422fff7e283f20c622124fa750b7cd1d579373d84084fcbcb370`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:19:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:19:27 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:19:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:19:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:19:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded11d00e86e206ca946f956082b11312785a0ffdc41ac54f6cb4d8c71dded2`  
		Last Modified: Tue, 03 Feb 2026 03:20:06 GMT  
		Size: 145.0 MB (144966615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b555fc99c59d3b28034ba76d7800409d027bf94e4d94a84e95500dabb371332`  
		Last Modified: Tue, 03 Feb 2026 03:20:05 GMT  
		Size: 81.2 MB (81150424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e54e3d82d3dd194fa82f8c29feff79a64f31a7896bae00c95efbe1089545026`  
		Last Modified: Tue, 03 Feb 2026 03:20:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:150b097c3b74df3283932cbda195660ef4af1b95edff73af2cb3566e71e7886a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cbceaf4bb71b8f608b664f936829a07cee232b8c103af0f07942e1d7d6bfbc`

```dockerfile
```

-	Layers:
	-	`sha256:8c1a3bb60a9ae5a6730ef1ccb423d24e76358c7be613ef3635645b98c9c0dc46`  
		Last Modified: Tue, 03 Feb 2026 03:20:02 GMT  
		Size: 7.4 MB (7395676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbe2ac1407f25cb00d334d5b6200129309532ac78a6a190b507f68169a463c91`  
		Last Modified: Tue, 03 Feb 2026 03:20:02 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12fe27cf20ccfc6005a593835535a7f63fbd844915d51b7bc0b5d74fce08fd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271234905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa0aa4790cd8ed907fb73e62da0c0022f2ff537db0bd2a1e1491e5bcbcde5e8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:04 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f037a921ffd807ecf95b4894a5bde495ebda17161e51ce5e5f31c195102ad11`  
		Last Modified: Tue, 03 Feb 2026 03:22:45 GMT  
		Size: 141.7 MB (141729908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2ff3016e210a6d0de5ada706156525fa2106ca32b9b0d245f7795a829edbb9`  
		Last Modified: Tue, 03 Feb 2026 03:22:43 GMT  
		Size: 81.1 MB (81138394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2288eeb21874964f66d3049da061aa51a0951deff8faf7b4a9f197e65467331`  
		Last Modified: Tue, 03 Feb 2026 03:22:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0732bf6091270f8fb6454f750657675a12eb50d88d87c9d51634c2a2ed1fa9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39b28f923be25c293ec85c40b5c4a6112d11834e09fc2e22c24649ed2519ae`

```dockerfile
```

-	Layers:
	-	`sha256:062a8a2bd4b7c1f74666829f7d79b2947f9d5488c815a540a15d8c1e4bdb088c`  
		Last Modified: Tue, 03 Feb 2026 03:22:40 GMT  
		Size: 7.4 MB (7402057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b52b371ec8ad6b61d2f1ba8868543d1b6086cd57301538fe28f8874aebaf6682`  
		Last Modified: Tue, 03 Feb 2026 03:22:40 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:322b4695d87f6762f4ba913d3c9b9316b3d961ce940beb89a3eb201be580e15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271394953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58467c6bd29c480632044d563cd99287d7abc026a9d7e61403abe953fc9ebbaa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:16:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:16:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:16:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:16:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:16:50 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:17:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:17:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:17:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ebe14f9bf3bd6292d3005c52dcc6a3a34db873e59d856fdb773a8f3f886f37`  
		Last Modified: Wed, 28 Jan 2026 18:18:13 GMT  
		Size: 132.1 MB (132079737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c579aa025f68231a24d525bc8ca88d1a0f8d820357df3d87cf43eae1e2d5`  
		Last Modified: Wed, 28 Jan 2026 18:18:12 GMT  
		Size: 87.0 MB (86987195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4984f6e20f1002caab2c0d3cc35b4833dbc7f63bfbd58a2dc51ab24b0e4a4be9`  
		Last Modified: Wed, 28 Jan 2026 18:18:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9dbf3afeb6037b4d8ac81a56b91e9f1e902b4794c9c4def16e07e866274ed3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b080c2bbbcc6d2670e2fe17cc52d10b18c59fea9ee3b18d17fb63f471ab117d`

```dockerfile
```

-	Layers:
	-	`sha256:fedec7854420d231bf7f4dea2d058f55694ce91765b254aaaa2fa8d2aa0ec15b`  
		Last Modified: Wed, 28 Jan 2026 18:18:08 GMT  
		Size: 7.4 MB (7400277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8371256abcd502fc384017a3e97bd6a167cd95c683a18b451aafd52454e692da`  
		Last Modified: Wed, 28 Jan 2026 18:18:08 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c7711cfcec1273d6d330afc7729dcbd4995f9b96f7f7c775835d1cf35fe8531e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252797132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34809e7b17ac59ebaf746344101eea6d8c05dba7a30f07ae379c43b50251de5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:00:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:00:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:00:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:00:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:00:43 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:00:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:00:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:00:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b29a4ec0282a03cd1a86ca27d6c7c588e1383f342a7ae9a4f8daf5fd965cde`  
		Last Modified: Tue, 03 Feb 2026 05:01:27 GMT  
		Size: 125.7 MB (125694867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce54db4e83c102dbefbdf1cd6b2ad75a9e065ac14e976556322d09a192ba886`  
		Last Modified: Tue, 03 Feb 2026 05:01:26 GMT  
		Size: 80.0 MB (79963276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeef392f44caf1577767855563b3c522effb5934432206f24e6740a9b4d5bf74`  
		Last Modified: Tue, 03 Feb 2026 05:01:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1a2310607d0fe3b75ec712678139daa8c6b7929120b2e600b4e7edd9ea07f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cafe1611ccc39a140e07f907da6bcfa4a0dd7cff8e0f94664e7315428311b20`

```dockerfile
```

-	Layers:
	-	`sha256:bd6b5b3ea2201611cbead1f793ec2acbd2a5acd856b934c1323c6c249d31f832`  
		Last Modified: Tue, 03 Feb 2026 05:01:25 GMT  
		Size: 7.4 MB (7386999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbba6acb2f9d0332895576dadf790abd0e34abe0c9767a6eb0adb60b23a0e96`  
		Last Modified: Tue, 03 Feb 2026 05:01:24 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
