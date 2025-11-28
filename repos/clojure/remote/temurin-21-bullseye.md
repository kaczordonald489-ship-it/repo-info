## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:90f28b76a97f7b2d51549eed399fb688b69e849564ea9d4f9d489aaf0a1d31b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b3b0fe4c719a204ea8e6b5e0911eccbad2abcb1254e9d937a59e91eac9873376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281144518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958289ac3812b28be7e333d77ea0633e7b2d59524bf73e4d1987ae45cf01195e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:13:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:13:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:13:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:13:54 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:14:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:14:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:14:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:14:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:14:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07abc57eb0fe9420ec1ada652a72e2890179f5ebe5b08e61eb94f0e8760edb45`  
		Last Modified: Tue, 18 Nov 2025 19:14:20 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65d92f0acb285e26cdf16ee90cce39d70d08797c8af93be635c3889838f199`  
		Last Modified: Tue, 18 Nov 2025 06:14:44 GMT  
		Size: 69.6 MB (69561020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3a6d132608fb44eb251d22d4060f377abadafe9f403d533cefaec739ba2af`  
		Last Modified: Tue, 18 Nov 2025 06:14:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d045e70bc95f224e0a08b031558c8bb9599cf75c78d7601a2742ed85388b18a`  
		Last Modified: Tue, 18 Nov 2025 06:14:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a95b9a51c93caf94d152cc7bf665b30852121ff6c54b1c6976291e98b99c269a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14da10c070132a48b218a4962c05678a355234dcb39d775e089f92eb23cb32a3`

```dockerfile
```

-	Layers:
	-	`sha256:441cd09c00a716536baa17e54bf633cfc15eaf47c4fdc1a3312d5a69abf58924`  
		Last Modified: Tue, 18 Nov 2025 07:44:03 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0340c5b8b9f56ed90c0c0d1ec8bc403cca8047564b66ad6c7b79d646c8ae73`  
		Last Modified: Tue, 18 Nov 2025 07:44:04 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a26364611b191bc251c76e219342e8e18f8a232ecc8e7545cefb0c13e1db969f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278054549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9beafbeff57bd6350b88a0062812a852a85f4a6979983a379472927175b36c9b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:09:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:09:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:09:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:09:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:09:38 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:09:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:09:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:09:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:09:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:09:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a154d1b83305c3d65122171509951d07d6aeca96ffa924f09f2ad91fbfbcd`  
		Last Modified: Tue, 18 Nov 2025 17:55:26 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003c95c55ce8fb890292c339c90f5535fc72cd68b605c080ba4874b6be475c88`  
		Last Modified: Tue, 18 Nov 2025 05:10:26 GMT  
		Size: 69.7 MB (69688237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0f8e04ad877fceaf4fff451d91dfc8d3a1f2856ea0b1b98627adf03431ed85`  
		Last Modified: Tue, 18 Nov 2025 05:10:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcbd269822a0b14b7ba8821356d21670078debac039997573bf22249be01754`  
		Last Modified: Tue, 18 Nov 2025 05:10:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9de5f1f7324dc6551adaec0a6413b8d44a7424ba548681c540147d5d61932b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97a0372300023a963a0682babba646a2aaeb5c97ea25a691124a59a0a02c8fd`

```dockerfile
```

-	Layers:
	-	`sha256:42eebfddd982df970922033dbe17c878377e84066aa3aaaf50dbf5ea985f938f`  
		Last Modified: Tue, 18 Nov 2025 07:44:10 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd53af11ae9e0bfad1bea351faf99c4993f9413a7a87ad017a8a92be5107079`  
		Last Modified: Tue, 18 Nov 2025 07:44:10 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
