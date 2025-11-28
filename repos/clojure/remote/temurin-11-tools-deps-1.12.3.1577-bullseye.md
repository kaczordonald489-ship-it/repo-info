## `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:b4f5dbbf1f4d4baf43a7170df5b925a7be12877a71624914c98a44e88203df45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:040c0d4eaae7baf391d6e33e3609eeffc23e05e50c630ba5a3763269e7cf8661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268284683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9bb06262e84bcc38be2daaa7a02a59fe0e865a90671cd915effdd25b73c631`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:08:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:08:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:08:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:08:06 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:08:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:08:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27894c18846b56d0ae56b24a85400623bffa3b5ea94988d3cdb4dd0ae3f77d49`  
		Last Modified: Thu, 20 Nov 2025 03:15:28 GMT  
		Size: 145.0 MB (144966651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e57b300894e4c0c503f8d32f277fda55faa368cf7442f77f2e3c0b07fd1494`  
		Last Modified: Tue, 18 Nov 2025 06:08:59 GMT  
		Size: 69.6 MB (69560957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652a9a75c8741c5f0ac4324df35bcd9c752c8d86cea3f4f6a6a9b3c2940566b5`  
		Last Modified: Tue, 18 Nov 2025 06:08:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cd735588513ba8ae20eb411e96ee77a03f0741a033bb1a12ce066a29d7aa070c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afd10eba7e7e4fbdbb9704e37ea22e8169d669959dbe71ec37ac523dc37749b`

```dockerfile
```

-	Layers:
	-	`sha256:8705f86872efb99581262822f98686f07e6c26f626d93e4ad90110d3883fde1d`  
		Last Modified: Tue, 18 Nov 2025 07:37:34 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d6b3016e0b2571fe3f33ff4eda236be99fa6dfb7da75f6b874322196971f9c8`  
		Last Modified: Tue, 18 Nov 2025 07:37:35 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7cb095f93f49e818c31f92d3b8529f0485f117558c00a271088121e96964b161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263677933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abe76b126046be2d252af3a79f3a8b77e1f867816366120a896a26bdda2214f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:58:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:58:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:58:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:58:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:58:52 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:59:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:59:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:59:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f82eab5f8d36d421014fcdd2fd02543fb16b57bd95d1ecbde4a4b3a53f200a`  
		Last Modified: Thu, 20 Nov 2025 21:22:49 GMT  
		Size: 141.7 MB (141731579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e11e5b7186bbb595fc5bd92d4212d9d3b810141f3052527a2947ae846d01ee`  
		Last Modified: Tue, 18 Nov 2025 04:59:42 GMT  
		Size: 69.7 MB (69688015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f027df07089f9ab60c792e861b8fd2fedc85d107c421888ea54630404ef87f4e`  
		Last Modified: Tue, 18 Nov 2025 04:59:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9238b2c71aa01aa15518e8fedfa0e3e4b887690f52afe61867291c01b970741e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f432b0f663d754a2ed4b7d90ba5b1065c398a8d1cad8ebb4bd8b5b43d513494`

```dockerfile
```

-	Layers:
	-	`sha256:01b45549a27a1c8cb442664363205de38b4ca5fc5f2f7d7473e305c4d227ed1b`  
		Last Modified: Tue, 18 Nov 2025 07:37:41 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b4f924501a149b54a86b9a9be27ce8b9c7baeef32a995befc4a027dc277560`  
		Last Modified: Tue, 18 Nov 2025 07:37:42 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
