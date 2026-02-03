## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:3b1e21f6203a26239f3a57b3288271478357ec6ae38b6025a3201d996d11d639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:f030adc35d092d7bded85936b1a7fa9c106e3ecf8a360fbaa8bf70cb7d546636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.8 MB (550757269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80d4523f6f12a992064823fd3ecc466fbf3f8b47e1cd90f82b8cc7f22828bf1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:47:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:47:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:47:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aa53a477a26c7392cdaa8f057a87c353eed9ebc4883b9991b23fada6344626dc NEO4J_TARBALL=neo4j-enterprise-2025.12.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Feb 2026 02:47:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
# Tue, 03 Feb 2026 02:47:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Feb 2026 02:47:11 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Feb 2026 02:47:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Feb 2026 02:47:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:47:46 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Feb 2026 02:47:46 GMT
VOLUME [/data /logs]
# Tue, 03 Feb 2026 02:47:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Feb 2026 02:47:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:47:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b476c8fd651f066240408ae1d37f16ff33ca750b88195f52ab3059226a6609c`  
		Last Modified: Tue, 03 Feb 2026 02:48:16 GMT  
		Size: 157.8 MB (157826065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54df5d832e91a7ba7938ecbfe2a37be38fd3737e8a46826cf5333427901031c`  
		Last Modified: Tue, 03 Feb 2026 02:48:11 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1618ec49c5084bbf3875c2f5a03c3abcaddfe04a5eed9485b940771f6a2804f`  
		Last Modified: Tue, 03 Feb 2026 02:48:11 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5e20fdf1312a74da6933690d368b9413f5ff26d2d18da18afc7671a3f0bb9c`  
		Last Modified: Tue, 03 Feb 2026 02:48:20 GMT  
		Size: 362.7 MB (362659027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d890f83fb83a8785e6265ca24bc720cb8514087ac5b83738f6c6cb722cfe10ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4871534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1af20a3ad2c28e2335e11c9c42f600492cd19fc54dc14e6089e52a6c89b4b98`

```dockerfile
```

-	Layers:
	-	`sha256:ffb546058efb9b58cf43a0a550c3c100e561728b52e835b498261541a3b72761`  
		Last Modified: Tue, 03 Feb 2026 02:48:11 GMT  
		Size: 4.8 MB (4849873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0837024393ea9a991d196a52d3654662d4c4efe7ec8b8e17576f4f130ec7291d`  
		Last Modified: Tue, 03 Feb 2026 02:48:11 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a32a24e43b21b1c61d4c247382d94959a1869c62b1cebe8546fa4e03adc916b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.8 MB (546768875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cad037ed22b769539f21eff0f8d501469458dbbc17afcdbd91771ed163d5a75`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:49:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:49:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:49:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aa53a477a26c7392cdaa8f057a87c353eed9ebc4883b9991b23fada6344626dc NEO4J_TARBALL=neo4j-enterprise-2025.12.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Feb 2026 02:49:56 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
# Tue, 03 Feb 2026 02:49:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Feb 2026 02:49:56 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Feb 2026 02:50:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Feb 2026 02:50:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:19 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Feb 2026 02:50:19 GMT
VOLUME [/data /logs]
# Tue, 03 Feb 2026 02:50:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Feb 2026 02:50:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:50:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067bb3bbe074612276c9f939e8d48692e24f69f52f44cd55f565c383c1fd03b6`  
		Last Modified: Tue, 03 Feb 2026 02:50:50 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e252ab8b9c58d681683d65ac382a4c86e68570fdd012595501931867929c6632`  
		Last Modified: Tue, 03 Feb 2026 02:50:45 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b89ff741c55550208530271812f15d022a30304c4997e6c32321b9a01ac616`  
		Last Modified: Tue, 03 Feb 2026 02:50:45 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e2cd30f49882c17495cd3808bb270e9fb580c7542945343971df22ed66877`  
		Last Modified: Tue, 03 Feb 2026 02:50:55 GMT  
		Size: 361.9 MB (361902868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a5652aa4920c41e7f6b16a0aadc5d420671851787fc27f1ed99395482676f3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4845556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797684fc4dc2e4a74167b8ae551f7fdb4805c138cdc0d769eee7120cd56bb72b`

```dockerfile
```

-	Layers:
	-	`sha256:29377f684d61161261e710f89ecd1c62c2c2089acfefa37eebe20cd63884ab4e`  
		Last Modified: Tue, 03 Feb 2026 02:50:46 GMT  
		Size: 4.8 MB (4823702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a96fd465d80113e738e39b608ee53828d542a74fd5c4cbe2ef5b37102655372`  
		Last Modified: Tue, 03 Feb 2026 02:50:45 GMT  
		Size: 21.9 KB (21854 bytes)  
		MIME: application/vnd.in-toto+json
