## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:10fc929d077d15e3130ad1d70f94887c5371f619e4a78b292e478c24ac8d808e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:dcfe2258fe2c0aa6313a87d303ef76b5668068c29bf9fa1f42a17e34207d189b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279791691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f3f491d425db8e55293c85b3aab09f1faefdb45ae4f21ab5ac07c32afd1511`
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
# Thu, 13 Nov 2025 23:38:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:34 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 01:43:16 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:43:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:43:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:43:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:43:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:43:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:43:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:43:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:43:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:43:17 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:43:17 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:43:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:43:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:43:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6234bedec03f1970bbe313a42227eee8990212e2faff0c50c24d6b65569cbb67`  
		Last Modified: Fri, 14 Nov 2025 01:11:34 GMT  
		Size: 215.4 MB (215361371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e7a0a80fd2ed3dd530c288d36317917087e523f1d89ee130eb62dbbfefb3ad`  
		Last Modified: Fri, 14 Nov 2025 01:43:38 GMT  
		Size: 25.5 MB (25462016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf58980a4745c03b3265deac83ef2f5ab2de8343de83e2815fae9a0264e7f01`  
		Last Modified: Fri, 14 Nov 2025 01:43:36 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad38af01a86579c5a5471826feb04a453b2b46ed140eaf09c8e705b5a8b5aac`  
		Last Modified: Fri, 14 Nov 2025 01:43:35 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019811cb23d71b73c0f893a6b5bba9a6df5b47fe80365c66ec453160b058ef03`  
		Last Modified: Fri, 14 Nov 2025 01:43:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:0ceabced5d989c6b5cf963bf2314d3e882240a536242ec53b42dac8393bc1809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4336480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c3be72e6f48ea8988e7c810354a443c6c1aeb7d331fe5e215ba541e55dea76`

```dockerfile
```

-	Layers:
	-	`sha256:340ce240a93e5cbfefa546d3be42f779655a779d8b45bb752893546607a24d29`  
		Last Modified: Fri, 14 Nov 2025 03:32:47 GMT  
		Size: 4.3 MB (4319977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8da2bd9698df208364fb4fb2d81479dfb87687587050a4ae0ca40b12b4f51a`  
		Last Modified: Fri, 14 Nov 2025 03:32:48 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fc04ebdde6f2a6e3438ecf53a5cc43a8f68f98b4e1c20e2ab014d13c6d355d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277255489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46b2af1916bfb303a30b6155032e2a89c8ad29077a6edd4aab0c52a3a1ee274`
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
# Thu, 13 Nov 2025 23:37:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:37:34 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 02:00:14 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:00:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 02:00:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:00:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:00:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 02:00:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 02:00:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 02:00:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:00:14 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 02:00:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 02:00:15 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 02:00:15 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 02:00:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 02:00:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 02:00:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de66503469f216f4e354e241b67e7c5075062d6c64f31a9e765638e19acc091`  
		Last Modified: Fri, 14 Nov 2025 02:00:04 GMT  
		Size: 213.6 MB (213617827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a93d2b9d77717b074422bc22c6ce8bce516f50dfc7849180b846e7dd740a13`  
		Last Modified: Fri, 14 Nov 2025 02:00:45 GMT  
		Size: 25.5 MB (25532095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c3230d8ead4c51b209660c84795801fc7582fadbc4c06c5bcec4bfcd90e09`  
		Last Modified: Fri, 14 Nov 2025 02:00:42 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf6c9c44c9bc3184b719d16452ecfc4ce801dde56a3ed4c4f7eb42bb6cc2ca0`  
		Last Modified: Fri, 14 Nov 2025 02:00:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fded105bde294c4b3e0aa5aa489398d9156cab1edcf5e418b08351693eac35`  
		Last Modified: Fri, 14 Nov 2025 02:00:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:80d7510daa5299679df8e6f5294fdc6dce4877e2d95a32f605d483cab40df072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6162b3dddce90dd142b94a337e9216c9d3a3f24fd2892dc8d3e234d51c2ae4`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa32234bf7d1904f825ea1d1aa1f9ab9760042ea77f9854b67712e47360be0`  
		Last Modified: Fri, 14 Nov 2025 03:32:52 GMT  
		Size: 4.3 MB (4326499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d3698b2b782db932dd24eef845c8ba1c1bb7114893ec36f2de50d3a4415ab`  
		Last Modified: Fri, 14 Nov 2025 03:32:53 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:2dd0c4b6e749ac1c1cbb601ca96d5741c15b980f6a2997543f82f18a8f0728c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289847229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b748bbb03300400b0ab319f8220219d870957bec9f14914423d4477c0172b88f`
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
# Fri, 14 Nov 2025 01:25:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:25:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 14 Nov 2025 01:25:32 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 14:39:00 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 14:39:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 14:39:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:39:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:39:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 14:39:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 14:39:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 14:39:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 14:39:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 14:39:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 14:39:02 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 14:39:02 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 14:39:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 14:39:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 14:39:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc44e43c8e58b7a80c4c0a125b14aaf046d89720422f0223c0accff723e6f79`  
		Last Modified: Fri, 14 Nov 2025 23:46:00 GMT  
		Size: 216.3 MB (216312812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b0cda5503897baf0faa6c557a186fa3b653a87ef2facb71a5cb075bad76e3e`  
		Last Modified: Fri, 14 Nov 2025 14:39:55 GMT  
		Size: 30.0 MB (29986362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d9e1306cd0116da4418d935eb0a3a9f6094f168c021478450e237810b93e34`  
		Last Modified: Fri, 14 Nov 2025 14:39:53 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca3fdd8825cb2b026fb9ae0a6b7c5ea925ebc26aa5a05f5575b0fff295c1354`  
		Last Modified: Fri, 14 Nov 2025 14:39:52 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdd83d1cf5cef08f2f6ffa16c551afa06b84e479fcf554942132c25ea9d668f`  
		Last Modified: Fri, 14 Nov 2025 14:39:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:ea4f320a71b01b6a6d2358ebfb00e4232a464f25d5e31eba31cceda8a3f5ee31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0662e71298d7bdc83af14c50e45888cd419aeb1ccc11e145f35feac41e1e9d89`

```dockerfile
```

-	Layers:
	-	`sha256:ec832e498ef439a5e957a567201e5bba5613567a49a7dfade24568a70aef996c`  
		Last Modified: Fri, 14 Nov 2025 15:29:10 GMT  
		Size: 4.3 MB (4318989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd0d91a2c14303f3736022566e4be5b2e84e00f7a69523b89bdeff527543458`  
		Last Modified: Fri, 14 Nov 2025 15:29:10 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json
