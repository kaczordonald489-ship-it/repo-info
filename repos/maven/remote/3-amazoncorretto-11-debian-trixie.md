## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:fb4315d0e172881856a3b7e6c4be56e24f38028d1101c78ccaca354141cc5766
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:7fa5dabf81bc54f05c4bff8f390f7b3ce54c9e51a5efc11edd8f34803a91875c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241676093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e909412f268c90572431b246bc07e5675d281deb6dea5086dda0e60e194bf00`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:44:25 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:44:25 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 02:44:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Jan 2026 02:44:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:44:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:44:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:44:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:44:25 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:44:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:44:25 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:44:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:44:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:44:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:44:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4c4e0559b822ce1a1a4b796f63e638ac2b775023d5ce3943eabc6a83c48b33`  
		Last Modified: Fri, 16 Jan 2026 02:44:48 GMT  
		Size: 202.6 MB (202589126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068bfdc1955dcaf998d2d92326b2d52e46efbe8ad18eef66f00d63c2ce5199db`  
		Last Modified: Fri, 16 Jan 2026 02:44:44 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511137631923a7fa1d14dfb374b8b01a709f1b8732d67ea07598963667733a12`  
		Last Modified: Fri, 16 Jan 2026 02:44:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db88d044c183cd37160a4a850e760ae574cafaaefcdeae90da93906f3d98dd4f`  
		Last Modified: Fri, 16 Jan 2026 02:44:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:d40a4cb28f231e64bc36ae72ea3d1499e7539489f6c8452fcfbad960e33434cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c50aeb0ad26eb47858c89100bba10722e3f3c1bce02f0f2bb5e68da6564d915`

```dockerfile
```

-	Layers:
	-	`sha256:e5d5d89a1c52987e9eafa5e1efc84c679b62ff3ddc1b9854a4404aec8c035a68`  
		Last Modified: Fri, 16 Jan 2026 02:44:44 GMT  
		Size: 3.1 MB (3109818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7be2f948ec91ed705454be848019f58bc603bd1cccc81d613c280bad1ef1f4a`  
		Last Modified: Fri, 16 Jan 2026 02:44:44 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5ed8c43d8379efa2413ecba49e06bc8814860ffe7f1810b205efe85dc317bca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239013439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdf18d1af2751dde30d42b5f268d98d0d38f95333d113c8c05f8680f0815add`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:31:37 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:31:37 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 03:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Jan 2026 03:31:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:31:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:31:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:31:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:31:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:31:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:31:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:31:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:31:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:31:37 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:31:37 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:31:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:31:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:31:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6483b8015fb63e849a917b8678afef749515f6b9c19f77fa0f024818d29b3`  
		Last Modified: Fri, 16 Jan 2026 03:32:00 GMT  
		Size: 199.6 MB (199566110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9ce01b9b29939bd8b0d50534ec54fd2283a55a2fc300ace3266bbc81f4b942`  
		Last Modified: Fri, 16 Jan 2026 03:31:56 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0581af9419b83162c61e09b7b12dee89493017af3e987b5810690700d813b0c`  
		Last Modified: Fri, 16 Jan 2026 03:31:55 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2734890413f49d35034a8efd43a9e13faff065a8b2072820206c326a3731cb`  
		Last Modified: Fri, 16 Jan 2026 03:31:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:61f97765f8ae68b24880a371313929808813a863e603c0ad16a3dfb83d19b55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e268e5318eaa2665b876b96c1fe81d0c7afcdf7ad63956440bd03b0ef23a5af`

```dockerfile
```

-	Layers:
	-	`sha256:c63ed5f80c78e7e684a51f203a375f84768992475da2fb1880f83af34f71ffb6`  
		Last Modified: Fri, 16 Jan 2026 03:31:55 GMT  
		Size: 3.1 MB (3110118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333b6d60b8cc755f3319a82f87058b9da5a0b040713c4b528f869dc1cc8f0be2`  
		Last Modified: Fri, 16 Jan 2026 03:31:55 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
