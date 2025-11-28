## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:9c1ccfeace879b06069dcbea32dfb9112cdd1c7e24036f54097b7eb9880e3498
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0fab27c859cfeda974752c926b223f389cd48066ca924304812959533549b587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401733290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060faaa0dd9d449e8fc29f566c699b5525fc3f7b8ff651deeed0ec495ae4f7a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:18:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:18:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:18:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 18 Nov 2025 05:18:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Tue, 18 Nov 2025 05:18:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 18 Nov 2025 05:18:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 18 Nov 2025 05:18:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 18 Nov 2025 05:18:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:18:58 GMT
WORKDIR /var/lib/neo4j
# Tue, 18 Nov 2025 05:18:58 GMT
VOLUME [/data /logs]
# Tue, 18 Nov 2025 05:18:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 18 Nov 2025 05:18:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6ac20e7b226e24cd0581e8720cbc22afc481cb7726479d331990c222645860`  
		Last Modified: Tue, 18 Nov 2025 06:46:08 GMT  
		Size: 157.8 MB (157825981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdac4fb0ca9b827b5553cbe0282aec62d8a7ebd32e46dcea53ed63055b862b7`  
		Last Modified: Tue, 18 Nov 2025 05:19:33 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387ad413050147e50d90571f6c1517aed0109e5c3592a5c1e4d786ce0803c3ef`  
		Last Modified: Tue, 18 Nov 2025 05:19:33 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2042fa71ef89da4d4b49637aa44b3a803cd80383991239a5d6b5eeb3ef5be2`  
		Last Modified: Tue, 18 Nov 2025 06:46:17 GMT  
		Size: 213.6 MB (213634941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:266face60bde8a0df703686f852659007ca82765a93118ef42a9f5d9ef9ffdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4630359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09429a233dfac1a69232080403ee637494d48bd57da546d61084766632d37a`

```dockerfile
```

-	Layers:
	-	`sha256:bcaa7a54fe3104ac739a8df31efbf6b9938d1dfa366be81f8011d4be88a0e8ee`  
		Last Modified: Tue, 18 Nov 2025 06:43:58 GMT  
		Size: 4.6 MB (4606293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7f2e1bcd46e5a49693d335667efbd101d45943e27b990dbd945d8bbddfe15a`  
		Last Modified: Tue, 18 Nov 2025 06:43:59 GMT  
		Size: 24.1 KB (24066 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0e9707e90b2496d710dbbc31fcfb73e9f7b30efcb872700798d47ca37e272483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 MB (397746347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ebd0b64b746cf9f96e24fe5ce631768014a74e35c050fde3dac481a2a0d408`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:46:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 03:46:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 03:46:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 18 Nov 2025 03:46:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Tue, 18 Nov 2025 03:46:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 18 Nov 2025 03:46:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 18 Nov 2025 03:47:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 18 Nov 2025 03:47:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:47:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 18 Nov 2025 03:47:10 GMT
VOLUME [/data /logs]
# Tue, 18 Nov 2025 03:47:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 18 Nov 2025 03:47:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:47:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b93a7257bcb801534002c1ea90c0e0453bff0715f612e38fef954299ae053c`  
		Last Modified: Tue, 18 Nov 2025 06:48:06 GMT  
		Size: 156.1 MB (156107671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dd6a008f471b92741281fbfefad7e231a0e77dacbfa4c7a21a213999aa7020`  
		Last Modified: Tue, 18 Nov 2025 03:47:46 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd18754c73fc2ba49ee73656047b70f11bb78e076de4b8ed6048da035429c2b3`  
		Last Modified: Tue, 18 Nov 2025 03:47:46 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d424e62c38236a8fa14a70e3cb6e68b26ceaf8b978e0f9f54b0432506f5db`  
		Last Modified: Tue, 18 Nov 2025 06:46:36 GMT  
		Size: 212.9 MB (212876294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a3e950a13594629717867431f4158d81e6b07f9e1e364effae87a9e967165ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cd8ef8eaf24540528a1a1e3e17764b337397a8dc5e5183a4b2e6ed00d6566e`

```dockerfile
```

-	Layers:
	-	`sha256:f347e305ee2f1bbf15bb062482f24983969b485147fe5fc3fcce89bb57a2fa08`  
		Last Modified: Tue, 18 Nov 2025 06:44:03 GMT  
		Size: 4.6 MB (4580218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2be3ac982955de111d84ab4b1b5a828ba4a9c4bbed846cb9dfca68bb3e6c8064`  
		Last Modified: Tue, 18 Nov 2025 06:44:04 GMT  
		Size: 24.4 KB (24355 bytes)  
		MIME: application/vnd.in-toto+json
