## `neo4j:latest`

```console
$ docker pull neo4j@sha256:c64d8750884c95ae57441a103d64d08fdaf55265acc3af687aa8ec25aa77d0c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:5736f91417c8dc4589d79aeb0e47de3c08b7c097026bfaae94ac6b7f9d76d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404211020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b1e931580301dfed1f1ce07c2fe63977e441b3612c222a2dfb820a354a307`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:46:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:46:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06c3d7b6cb9532e3ec2c03f24d076e3acac5abfe6d7394f855910d2c12f7c542 NEO4J_TARBALL=neo4j-community-2025.12.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Feb 2026 02:46:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
# Tue, 03 Feb 2026 02:46:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Feb 2026 02:46:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Feb 2026 02:46:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:46:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Feb 2026 02:46:59 GMT
VOLUME [/data /logs]
# Tue, 03 Feb 2026 02:46:59 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Feb 2026 02:46:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f328492c273e3a25b7d16af8d467d17469346aaf44501f1f2bdcaa3a3a8d1bd8`  
		Last Modified: Tue, 03 Feb 2026 02:47:30 GMT  
		Size: 157.8 MB (157826065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bbbf06d66d19f3ac970bcea96549f24efc5d9db962bf0644cba557ce4320e`  
		Last Modified: Tue, 03 Feb 2026 02:47:24 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedaf1a1fb02b58b4521fe714d3f1e69ee9c1e44042b1d6f493e9131d0ea6122`  
		Last Modified: Tue, 03 Feb 2026 02:47:24 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0363cdcaadcad99d76b50f6ef10325a6bfaff3dda41bd3debfae02e1a3beb347`  
		Last Modified: Tue, 03 Feb 2026 02:47:31 GMT  
		Size: 216.1 MB (216112776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a7741a368ef4b4a113d950dfdeb9a9a0b43078a84a9a36963f8c9c06849ac00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6018a5f5f4171a7084e31cf6978d937fb5747b8003fcbc3a6437cfccf9e37c5a`

```dockerfile
```

-	Layers:
	-	`sha256:3294f3ce8c290a60231f078ca84241278829e23591b35d3b4e36ce0190320757`  
		Last Modified: Tue, 03 Feb 2026 02:47:25 GMT  
		Size: 4.6 MB (4607183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0eec38f7cae40e5157d3c89c740446c66b0edbe8eb8195461c513f81d63ad82`  
		Last Modified: Tue, 03 Feb 2026 02:47:24 GMT  
		Size: 24.1 KB (24066 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cc607e00e3ff8fe594b0b76bce55f48d68ddddd90d2756383ea3655396bf37cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.2 MB (400222828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925e8ecf1a94d32471a3be2b038559389ca032249d14e85f5ec0eb0b93b564f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:49:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:49:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:49:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06c3d7b6cb9532e3ec2c03f24d076e3acac5abfe6d7394f855910d2c12f7c542 NEO4J_TARBALL=neo4j-community-2025.12.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Feb 2026 02:49:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
# Tue, 03 Feb 2026 02:49:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Feb 2026 02:49:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Feb 2026 02:49:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Feb 2026 02:49:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:49:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Feb 2026 02:49:50 GMT
VOLUME [/data /logs]
# Tue, 03 Feb 2026 02:49:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Feb 2026 02:49:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6e74c6e4d25b0782b574b670fda91f2431b30e00b8d92ca55bbfb2a8f1ece0`  
		Last Modified: Tue, 03 Feb 2026 02:50:19 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809c4a6247c85b3e4da0335e7fc09c3df5991522ddefb63dde587ce4f4555ca4`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7560e339a583d4f73ccc355f5eb29771b32a2bea55987d5bbc678e3a9ec9fd`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7499ca303ef45764282da1265343955383412ed646cfc62b22ca7446ce31dd`  
		Last Modified: Tue, 03 Feb 2026 02:50:21 GMT  
		Size: 215.4 MB (215356889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:67ea81b232670eb6934f498978c43382c3a9a884f87ca98b337f1929e57d47f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b73a2b387dd848b371b0bfa5f7e4df892f481c4356a02278808098e8a0a1b3`

```dockerfile
```

-	Layers:
	-	`sha256:5c390d1821f59b84d088661e26359e8284baf2be20879aa583ed5f5782f0bd81`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 4.6 MB (4581108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253bd29db89cecf4d8b3c86d41ed5490825647fb193d143d370be856f75f185c`  
		Last Modified: Tue, 03 Feb 2026 02:50:13 GMT  
		Size: 24.4 KB (24355 bytes)  
		MIME: application/vnd.in-toto+json
