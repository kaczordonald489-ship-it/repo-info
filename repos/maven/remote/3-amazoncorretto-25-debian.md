## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:8c28e4b34b19500762ba671b6d9309bfbaafe828bf834a7cdc838ee23e684bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:a3ea2176201f82ef4084a3950ffaaf319d73ad9fbcab8685eba00f898a11cfa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274251740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0cdc564c91306752c59ae12c488832fe30e792e46c0642f141eb096b0fb636`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:21:04 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:21:04 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:21:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 18 Nov 2025 06:21:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 18 Nov 2025 06:21:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 06:21:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 06:21:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 18 Nov 2025 06:21:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 18 Nov 2025 06:21:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 18 Nov 2025 06:21:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:21:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 18 Nov 2025 06:21:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 18 Nov 2025 06:21:04 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 18 Nov 2025 06:21:04 GMT
ARG USER_HOME_DIR=/root
# Tue, 18 Nov 2025 06:21:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 18 Nov 2025 06:21:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 18 Nov 2025 06:21:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15484af55e71887f69825eba197861dbff9a567b03efb5e83cec95b2b3b9da62`  
		Last Modified: Tue, 18 Nov 2025 09:30:53 GMT  
		Size: 235.2 MB (235231624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c02f2fcb168eab8757545783350891e54a35798d177697541698f471d8e7616`  
		Last Modified: Tue, 18 Nov 2025 06:21:39 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036669b5e09c9476e3646ee4af2993c2b16fd34681acca08fa3b5a127dd25a6`  
		Last Modified: Tue, 18 Nov 2025 06:21:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c34c469dc2ee7027ce0b12690f79cf6b4082074f6f1c7ff543d6ced71a05f`  
		Last Modified: Tue, 18 Nov 2025 06:21:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:913800dbd870421024bffeea35536108c689c21918c606cb620144cd35e9913d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be628af01855cb1ea05ffb7e05a944e7013a12e323279cb9ebd443c591573061`

```dockerfile
```

-	Layers:
	-	`sha256:5691375805009f4699743f65d25f36a584e367e455534fc725e10c612325e691`  
		Last Modified: Tue, 18 Nov 2025 09:28:28 GMT  
		Size: 3.1 MB (3112961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc9e411fa381104f35cd535e56cdfad3efc34b48ae379cbf27cbd8885ae6bd6`  
		Last Modified: Tue, 18 Nov 2025 09:28:29 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8885ec2dd44da22039d76d5c17dbb41ac720120c21aed3bad624bce270bb4c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272348707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4377a9e495e6aada0438571fcaa349702548e14a7ea316a467d11014907de275`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:21:34 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:21:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 18 Nov 2025 05:21:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 18 Nov 2025 05:21:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:21:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:21:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 18 Nov 2025 05:21:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 18 Nov 2025 05:21:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 18 Nov 2025 05:21:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:21:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 18 Nov 2025 05:21:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 18 Nov 2025 05:21:34 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 18 Nov 2025 05:21:34 GMT
ARG USER_HOME_DIR=/root
# Tue, 18 Nov 2025 05:21:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 18 Nov 2025 05:21:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 18 Nov 2025 05:21:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07ea3c69a67094064792c802cabfa3bf1688404d61acc12c50e9e30525d464a`  
		Last Modified: Tue, 18 Nov 2025 06:51:05 GMT  
		Size: 233.0 MB (232966489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bcd11e5e0191298d631024341685a4e6efc098da350fe25517b12fcd66327a`  
		Last Modified: Tue, 18 Nov 2025 05:22:08 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1851332d1ca99016d3c4edc23171c5bf8e87ca2ac6b67f1946f0fcbeaa3dea`  
		Last Modified: Tue, 18 Nov 2025 05:22:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a40df74457caf5d1342ce9bf309e0c96cffe2bcd13cce1e194366179c4132f9`  
		Last Modified: Tue, 18 Nov 2025 05:22:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:208f896e55fed3955d45381612544570788eab2fe411dd4c8b677a0768f91519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6f9ba862c958a5b132f306c608bfda0d57c0596199d7a184c6ae92eb4206c0`

```dockerfile
```

-	Layers:
	-	`sha256:c080a2928471c587f60291dfd427ce05e4e07eb6bf0ac87f4cdb19ca90b756ed`  
		Last Modified: Tue, 18 Nov 2025 06:30:16 GMT  
		Size: 3.1 MB (3112621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be416f4da63c7eccae99562b5a46b8e224d772a859d28cf8becf068654891cb5`  
		Last Modified: Tue, 18 Nov 2025 06:30:17 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
