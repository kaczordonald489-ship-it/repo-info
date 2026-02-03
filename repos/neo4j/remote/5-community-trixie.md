## `neo4j:5-community-trixie`

```console
$ docker pull neo4j@sha256:f3d3feff59b84dd867490f1da11954b4ec6e86f4a9e2bd053c476c60541fa8f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:692330e73263caad1513ba08f0a4bcf26f13cce347332878f108068c586a980d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321178462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0363c185271200daaf1b6aa62205121caeb51abc09b099caaa01ebb6871122ed`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:47:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:47:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:47:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=38e5643bf76a8fa714421be8be2b12d6280b7f891b2d29ae16172e57de0e9432 NEO4J_TARBALL=neo4j-community-5.26.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Feb 2026 02:47:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.20-unix.tar.gz
# Tue, 03 Feb 2026 02:47:22 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Feb 2026 02:47:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.20-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       adduser curl ca-certificates gcc libc-dev git jq make procps tini wget     && addgroup --gid 7474 --system neo4j     && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Feb 2026 02:47:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:47:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Feb 2026 02:47:50 GMT
VOLUME [/data /logs]
# Tue, 03 Feb 2026 02:47:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Feb 2026 02:47:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:47:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b7c89406a93e40e2593f8d854fbf11b4d54a833e5e5f304ed8daa657f36496`  
		Last Modified: Tue, 03 Feb 2026 02:48:15 GMT  
		Size: 157.8 MB (157826034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6682408898b13c050c2aaf60a241afaaee4c6c766e89001ebe1d18b246eabd`  
		Last Modified: Tue, 03 Feb 2026 02:48:09 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce5330d37a878b0626031dc8c498e1360afa49e34055da0abad53568df7849a`  
		Last Modified: Tue, 03 Feb 2026 02:48:15 GMT  
		Size: 133.6 MB (133563738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:0242d88c47523461c06d6d6de4dc5e5b1c77687585229b748f5b39934926bf5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaef2d902fe135ecc13f4abb8adbb3f925eae9a0b60195c27b42a1ef2a489b3`

```dockerfile
```

-	Layers:
	-	`sha256:2692f3110a809e30417c2299a8068cfc169c23fc270120e086f87fea33873c82`  
		Last Modified: Tue, 03 Feb 2026 02:48:10 GMT  
		Size: 4.3 MB (4303401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16c4fcb95b56b9d891dc905bc3ae91d9c9a51188ce657547f3f342b8fdc301c`  
		Last Modified: Tue, 03 Feb 2026 02:48:09 GMT  
		Size: 21.1 KB (21097 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1f511c8610d85d5c47f3ab8c64e3a8d08961ff51078159df219c43c8cb214aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318895333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac60a0a97301c5e509a51fa8165e934e3425d832d454dd3c1a446417454d71f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:50:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:50:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=38e5643bf76a8fa714421be8be2b12d6280b7f891b2d29ae16172e57de0e9432 NEO4J_TARBALL=neo4j-community-5.26.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Feb 2026 02:50:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.20-unix.tar.gz
# Tue, 03 Feb 2026 02:50:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Feb 2026 02:50:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.20-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       adduser curl ca-certificates gcc libc-dev git jq make procps tini wget     && addgroup --gid 7474 --system neo4j     && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Feb 2026 02:50:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Feb 2026 02:50:24 GMT
VOLUME [/data /logs]
# Tue, 03 Feb 2026 02:50:24 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Feb 2026 02:50:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c5b4f8584f8cfcecd6e7cbd791c4dddd6ad84447e6fc4a757c0025a551c04`  
		Last Modified: Tue, 03 Feb 2026 02:50:49 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d882d1b8d590f4ea4b15406139f7c0a7aee4295c8376886b88f3e4bd6c112d6`  
		Last Modified: Tue, 03 Feb 2026 02:50:44 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87e83fa0d72190a8830a2583e3844a299b348f8bceaaca0874b322adc89690d`  
		Last Modified: Tue, 03 Feb 2026 02:50:49 GMT  
		Size: 132.6 MB (132637599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:09345a0531d105bc9f3e8d00fcbf2500087f1aee2788c1aeb0d0ad198234ab0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8a6ab77c90ad8ab069b8af577c073c7041c360c1add07907c3d219e4e066a`

```dockerfile
```

-	Layers:
	-	`sha256:c0b621a7fe11dbf8ba69ebf734e30543ab7beeb8fafa1ee4be8fd81cfd66667e`  
		Last Modified: Tue, 03 Feb 2026 02:50:44 GMT  
		Size: 4.3 MB (4297927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:164094cc56044d831c204ab0f74088e1004779da53d560cea84b7d10217be801`  
		Last Modified: Tue, 03 Feb 2026 02:50:44 GMT  
		Size: 21.3 KB (21323 bytes)  
		MIME: application/vnd.in-toto+json
