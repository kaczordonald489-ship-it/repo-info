## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:16c72faa78c55c19b9d914cd561d897810ba7bc155fe4e71b7a79a47264b4ec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1af14925416b60cffdfbe596c65f83a081aa66c71ae1ad895435cbda387f5162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215362006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef811f2b690ef29ee68317b4f5fd23b360b25d08d8fa4062520ac84be77861c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:15:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:15:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:15:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:15:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:15:55 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:17:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:17:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:17:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:17:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:17:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fabda67223a4194fa3462816183ec80e6a4ec1fbc8e1b42476a06147808823`  
		Last Modified: Tue, 18 Nov 2025 06:16:42 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f779b9da2db0ba03c54b359d8c1c75864424108f5f476a9dbd10bde9d14db252`  
		Last Modified: Tue, 18 Nov 2025 06:18:07 GMT  
		Size: 69.6 MB (69559237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b638164c330b373554994560a146309c548a26cb83a2a723aa45244287f8f`  
		Last Modified: Tue, 18 Nov 2025 06:18:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c8696c2dc3011be5361bec8f0528602e03aa2db7be8a829c33be6e5b05d8e`  
		Last Modified: Tue, 18 Nov 2025 06:17:59 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3a8f6e887b94e7d7fd6d5444b4c81829f2403aa3472d842cbd7cd7897ae78777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49bc37617b708a0fa028047abeb5c837a1dcd92ca54e997707b48de7be98ba3`

```dockerfile
```

-	Layers:
	-	`sha256:b08487a2914311a3f086fc5e89b8f6219e18eec9a9b8861f04f26f0d36344fa2`  
		Last Modified: Tue, 18 Nov 2025 07:47:22 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fba81320d572bf8c096aac51f17a8baabbf3f94c82a20791e722ccdb1b78b3b`  
		Last Modified: Tue, 18 Nov 2025 07:47:23 GMT  
		Size: 15.6 KB (15648 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dda6d8fc6e63cd63618efa4b96f7226e031c4edde635a19093af317d6ec52538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212999350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3fc2c5745595bfd36f23230b375a75e54265ed3439e228dc1e6d138ca5bebc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:12:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:12:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:12:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:12:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:12:54 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:16:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:16:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:16:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:16:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:16:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d3d88c171e228bf518ae34b2ab7dc7c4ea00ec7d81ebc15f3c2a53e89e942f`  
		Last Modified: Tue, 18 Nov 2025 05:13:49 GMT  
		Size: 91.1 MB (91052501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b0c0c195b5aaff81ee4a4c1d5fdabf6547e6ce1a4add77c9dfa885c0eeb10`  
		Last Modified: Tue, 18 Nov 2025 05:16:38 GMT  
		Size: 69.7 MB (69688111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa89ab7f9fff176b2a6279f1fabfe4ea1752e4025755d0ad4bd42bcb73d44d60`  
		Last Modified: Tue, 18 Nov 2025 05:16:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e576922669192d2557b01d8fbfe06b90aaa00dea9b09cb1651fa67162bb80f1`  
		Last Modified: Tue, 18 Nov 2025 05:16:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9ff0080a3409400db2e0e7ede0543d2164f172dc24e525fb7fc13b57d814289c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150bbfd58e401e1c7c9dcbbd52e88f7c1d33a34efc9c2254c3242b7c0953f64f`

```dockerfile
```

-	Layers:
	-	`sha256:d748cc0708cd452048c246eaac5394b90a9f69cf2ceda15f069c1d5fb535c501`  
		Last Modified: Tue, 18 Nov 2025 07:47:30 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da289a5e6fee356c7dccb05d6cae79d108c205619732604561efb1761910608b`  
		Last Modified: Tue, 18 Nov 2025 07:47:31 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
