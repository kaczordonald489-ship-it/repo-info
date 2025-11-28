## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:fd413e8da4d560208fb2d01459ec81f69ab383da68fbde18d28d431d7c3a4cd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-17` - linux; amd64

```console
$ docker pull maven@sha256:85f9e0bde2393d924789f8ac8b939929f063edb3f4649b9b8b7f7cf219439cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265099401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8fc99ff0a8775459b1d1d62128da3410f6a693377b6595b8c3399cdae2e8c9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:01 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 01:43:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:43:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:43:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:43:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:43:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:43:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:43:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:43:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:43:08 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:43:08 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:43:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:43:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:43:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631b1914a3f666b03be170977fda73e9d2f60cdeff1977715823aa31a3ac6184`  
		Last Modified: Fri, 14 Nov 2025 01:08:08 GMT  
		Size: 200.7 MB (200669076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ce4c3e40caa0b71cb9dfe7ead2d09547a5f55cfdae0af8dfbe9aa83382e425`  
		Last Modified: Fri, 14 Nov 2025 01:43:33 GMT  
		Size: 25.5 MB (25462025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd245e7177a445de6bced343fb84855cacd2bceda94c3b43c6ebf171cc2b2a2`  
		Last Modified: Fri, 14 Nov 2025 01:43:30 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74fff785fd95ad998d1759195d7584ddee993ec13488ca1506c8469e37c2fc`  
		Last Modified: Fri, 14 Nov 2025 01:43:29 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119791d8f03bebdae67bf4e6d91777a7f3c9c4f896ed857a558e7e18343b5cb`  
		Last Modified: Fri, 14 Nov 2025 01:43:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:410ac181915877765b9469a4b361dd3298a3499c91c3bd41601213a65d341d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4334613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1765dea50fbad2d4594e43b5659fb56dc71b297ec54b63ca3bbfb199a0d0de5d`

```dockerfile
```

-	Layers:
	-	`sha256:f9e9609f071fb5d85cb497a7697c6498809e5b261de1e68506f512284fa81115`  
		Last Modified: Fri, 14 Nov 2025 03:32:37 GMT  
		Size: 4.3 MB (4318110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ba94bc56d29a7d3330c3bf3e6567672ce267c5be192874df52b3e7aea6e00b`  
		Last Modified: Fri, 14 Nov 2025 03:32:38 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:471287322251a2476beb00a602914b59838030896b2455bc28a1ee5711001d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263029663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1b40e927989d00c33a5f52ee767ae1bfa76e42bdd6c61bef669a1180f3e100`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:38:29 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 02:00:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:00:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 02:00:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:00:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:00:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 02:00:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 02:00:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 02:00:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:00:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 02:00:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 02:00:09 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 02:00:09 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 02:00:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 02:00:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 02:00:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83709b1cbcef0ca40d50087b6293d8e8293235be7fe636e4c606ce2dbb43e6b`  
		Last Modified: Fri, 14 Nov 2025 01:59:45 GMT  
		Size: 199.4 MB (199392164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695804c55a20c7d62e5795d2d27074b4d63c163710a807a9a49e4618230c981`  
		Last Modified: Fri, 14 Nov 2025 02:00:37 GMT  
		Size: 25.5 MB (25531929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c47453aea4e103d318c61d7c40969984d29ebbde73bd2c67361e3525f00615`  
		Last Modified: Fri, 14 Nov 2025 02:00:36 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b80260ec1ce03c1163368370babccae0585f8ed966a39b0ded1917eefd0a10e`  
		Last Modified: Fri, 14 Nov 2025 02:00:34 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a91bbd5e4d2844f57af2d3d28a7cfd4c2ee1e3a453ce2ed843cfb7e8ceed9`  
		Last Modified: Fri, 14 Nov 2025 02:00:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:c0a996d4f05908803a8cbc6af16f68a6c8fd3b4e9acafbdf613c0f4cb04b901f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4341268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd08812f38686dc8d38b7b356ac436ec6f7c6cbb73fb3e6b510bc1f53be89ab`

```dockerfile
```

-	Layers:
	-	`sha256:df70c1a6f3e55936b1069b1c9380cfbe8b7a3ff8558d3b6b4638e002488d5742`  
		Last Modified: Fri, 14 Nov 2025 03:32:43 GMT  
		Size: 4.3 MB (4324632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35ce79398dea62b9f6dcb12e4cdfd85e317ac30dcb165e441bde216dc63f231a`  
		Last Modified: Fri, 14 Nov 2025 03:32:44 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:97a1795bdf83d150061b5af6855ad52afa8ea45aad606d63cbf3d56077e55fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274989414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744aa964a724b45703754e392d96d8f3988b24d564ef16e082cd03e8759d680a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:42:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:42:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 14 Nov 2025 01:42:47 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 14:37:42 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 14:37:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 14:37:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:37:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:37:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 14:37:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 14:37:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 14:37:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 14:37:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 14:37:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 14:37:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 14:37:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 14:37:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 14:37:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 14:37:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf9450fb1f80147f4cd24e5f6ee622cc8c41793888ad7d7b656ecde5212a68`  
		Last Modified: Fri, 14 Nov 2025 17:18:49 GMT  
		Size: 201.5 MB (201455205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a56477b5dff001ba2d3961afab49795167aae0b70ac4fbdaa3184c52d8fadf6`  
		Last Modified: Fri, 14 Nov 2025 14:38:34 GMT  
		Size: 30.0 MB (29986171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbabb4ea6c19ff55853bb74667b184f430c3c887455b3c00a959b2cb7fc5538`  
		Last Modified: Fri, 14 Nov 2025 14:38:31 GMT  
		Size: 9.2 MB (9242574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd0cfd0ffdd74da652170f120de6f73791c593638ff9740bcb3ec3906ff7d30`  
		Last Modified: Fri, 14 Nov 2025 14:38:30 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef62cc33b451f8cea8804e7d086beb58ce78d3ff525a064c81c575bc0bb3f1f9`  
		Last Modified: Fri, 14 Nov 2025 14:38:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:8da92f1232ecd0238ae99fb4f31d885f999954ca55f506e17d755f9ad4acb0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7b57c3ad3368def3de48eaa78512c25d4a80c24bb08a12d3a4e26800c10785`

```dockerfile
```

-	Layers:
	-	`sha256:b1405b116da0ce4d746ea85fe10ff6bda3c64629fc99ac73f098c9afb48b5ca5`  
		Last Modified: Fri, 14 Nov 2025 15:29:06 GMT  
		Size: 4.3 MB (4317122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9d2e2331999584449b37a06f85521c463ab746b52e89b8ebe7863dee2a17a7`  
		Last Modified: Fri, 14 Nov 2025 15:29:07 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
