## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:eb17396a8027552fe9a2825617441e19b06eecf43797bc5ec57505d9efdf75e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:06c90a38596c86311b2dca16a16769c644155958f711f935842e4e2f66e64c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255621875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9652166d31f7885751f750a19676e49e5f7f9ec5cb71a23fd8ae721b36d6c47`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:20:05 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:20:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Nov 2025 06:20:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 18 Nov 2025 06:20:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 06:20:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 06:20:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 18 Nov 2025 06:20:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 18 Nov 2025 06:20:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 18 Nov 2025 06:20:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 18 Nov 2025 06:20:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 18 Nov 2025 06:20:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 18 Nov 2025 06:20:05 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 18 Nov 2025 06:20:05 GMT
ARG USER_HOME_DIR=/root
# Tue, 18 Nov 2025 06:20:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 18 Nov 2025 06:20:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 18 Nov 2025 06:20:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def3bea4664d37680d5ec00116f4ddd5029f70d5384437cabacdca2dec7753e9`  
		Last Modified: Tue, 18 Nov 2025 09:29:34 GMT  
		Size: 216.6 MB (216601784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f945d1c92b77de6cf2b4980d15d4f11fdd229102a4bbde874e6f4b429b03e9`  
		Last Modified: Tue, 18 Nov 2025 06:20:37 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd79442fcad4275cfa5e146d0809620e007ad018ab1b50946b26b38ee83f75a1`  
		Last Modified: Tue, 18 Nov 2025 06:20:36 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc202024fc32d8013437451c0e4d427ae07ec09ea5eaeb8a7bd7aec3c439597b`  
		Last Modified: Tue, 18 Nov 2025 06:20:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:96ed3fcff5ee25c8aaf07c1442ff168f5eb5cdcfa0106fe6bc4e28c829b77bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6005ad24525f93e5dfdc8ddc699a3e1fe3da5d635ce0cbdf99939e3116ddb3b5`

```dockerfile
```

-	Layers:
	-	`sha256:f89a4cfcb50832238731ff106d60e3dd22015cb76d78fa02083ff02967a3d660`  
		Last Modified: Tue, 18 Nov 2025 09:28:18 GMT  
		Size: 3.1 MB (3103861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0b01657a07587f260eeaa1ed7bfdf2121d844769722612334c80a7e132c178`  
		Last Modified: Tue, 18 Nov 2025 09:28:19 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7f8da75916cd7269ea407c2de312acfa179b85dc26382fafe90a3ffc89d63c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253937543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d02f13b87faa9e90fad7d8f894e9ba54eec8e5f8a37d61e4089ff0eb39721ae`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:19:26 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:19:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 18 Nov 2025 05:19:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 18 Nov 2025 05:19:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 18 Nov 2025 05:19:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 18 Nov 2025 05:19:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 18 Nov 2025 05:19:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 18 Nov 2025 05:19:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1833ca47eecf2eba86e5db679913b120d30cd04b05d1bb4b3ea0ad0fc162f69d`  
		Last Modified: Tue, 18 Nov 2025 06:43:38 GMT  
		Size: 214.6 MB (214555302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd7e0497a65b5350b2cdaf258d649c2deeb8d374610dec7ac91c1850bc8cb82`  
		Last Modified: Tue, 18 Nov 2025 05:19:58 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb192418d371baa3123f61419858e6f6ef668a7b92d3e473819bb4ba64f7161`  
		Last Modified: Tue, 18 Nov 2025 05:19:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0371a83b8f3023f2826730ac08cc84f39ce6fa0b5b8739ee32a39a94eb227210`  
		Last Modified: Tue, 18 Nov 2025 05:19:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:3aec602683d81f0065684c68b72f4ac0e4437db04d5c2dfe635559826f844866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea815ee3755d0a42ee412df55cac6a0797ba6bbaf720ac2554d9db827edd7ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b517d2fa8a120ec7aa9b3efb902b19001274fbbb96935fa8f054d05c562a0dc`  
		Last Modified: Tue, 18 Nov 2025 06:29:15 GMT  
		Size: 3.1 MB (3103524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe8d5698ea57132cbadff0b56d774eb2e213a6c5ece1f0bef2dba0c6fa07b59`  
		Last Modified: Tue, 18 Nov 2025 06:29:16 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
