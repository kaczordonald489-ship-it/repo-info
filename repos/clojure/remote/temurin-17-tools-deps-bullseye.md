## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a80dc1cf56987d003e2e7b9161a697d61b404b5f4dfaffd2c2e36d041a0877d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ac913cb188044fb4913b83de49fe985ad3d2b5ef5e600545b931ccb69d68654c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612950772f8ea87d4f3907bc24329c866babab05e5e88182a24f017761b026e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:10:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:10:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:10:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:10:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:10:00 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:10:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:10:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:10:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:10:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:10:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159fcf230eb58fe739c590a3424e4768eb61e57b0c34ebc01e9341df918930a8`  
		Last Modified: Thu, 20 Nov 2025 03:53:28 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb671eab02e802c6d2e1b59bce26bab564aa60110649acefc9e097e3daf3dde`  
		Last Modified: Tue, 18 Nov 2025 06:10:49 GMT  
		Size: 69.6 MB (69560620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72865c1622998247962989fff2324fb2dfb22db661783b839f292b0c74f2e829`  
		Last Modified: Tue, 18 Nov 2025 06:10:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a45083c7b2eb1b267aaccdc855abcb9eb4b8a78da5017ce5b9ffb91fd430`  
		Last Modified: Tue, 18 Nov 2025 06:10:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:85faee3f4280c79c5b6299de35556a6c5cfbcd13147a1e0b47bbb4444425c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766da35a20d45d680352682b64e87dca8cdc550fac5d505cc119cbbf4c79bef2`

```dockerfile
```

-	Layers:
	-	`sha256:b178fbe394b6b1989804846953716407be09c95131b54be7595a28303a81dd05`  
		Last Modified: Tue, 18 Nov 2025 07:40:49 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b02ad58010ce1f7ace015a59105e9df2a5fe732fb72a156815c380a91acbd5`  
		Last Modified: Tue, 18 Nov 2025 07:40:50 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f379267fd742e7a349cf1409aca484f6f1618a55615baf3cecde1bfb868730bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265626848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce69d9d0e3c4d9f022482936ce434f932a2141f7f867c83748d28080c203739a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:04:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:04:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:04:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:04:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:04:14 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:04:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:04:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:04:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:04:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcd68db7b50986b9b255fe942cf8015ad9d73ed481fd7d3a0dcfc77afc78748`  
		Last Modified: Thu, 20 Nov 2025 20:12:22 GMT  
		Size: 143.7 MB (143679915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed38c8c5211179b58b681b8fd8a37891df74b3e9e15b661db7d6b72aedd259`  
		Last Modified: Tue, 18 Nov 2025 05:05:11 GMT  
		Size: 69.7 MB (69688198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4902a5a7f3a368c2738db2d7a4bdd220ade0bc87b52f2f8651e139d1ce198`  
		Last Modified: Tue, 18 Nov 2025 05:05:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d705b07eb2e4d940fd0ef1e5d367a5794b1c90e4ab9a6bddb32961c860bc0c3`  
		Last Modified: Tue, 18 Nov 2025 05:05:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fe6a34fe1b10b4c6667c782fb0ce286b9c5146f5e63168446646c99aa908076d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b39782346f024c9e7c40b247eef65167bbfdb63dc8548481e58d84651e8d706`

```dockerfile
```

-	Layers:
	-	`sha256:b28025d3ff9673b0fdb907813076a635d5a57d26d3cf010d51b60f693d297866`  
		Last Modified: Tue, 18 Nov 2025 07:40:57 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939873e21289c6ea642d31526a3abee1ad9e230d3ba06379f92c28eb8d8b6c96`  
		Last Modified: Tue, 18 Nov 2025 07:40:58 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
