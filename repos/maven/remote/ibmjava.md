## `maven:ibmjava`

```console
$ docker pull maven@sha256:cda666a3d85b644102197ba9f2e44e4188295ee703a6fd7e4cb5aa1f6e4b7e92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:67e6ae5c679e501920c58f3099b4e3b988401928410ba234a37d6b5082bb3a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216129033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c55de7d1a401579593c98fb21cec88b6fc017c48e0beefbd438da4d5a53b93`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:28:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:28:03 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:28:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 14 Nov 2025 01:41:02 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:41:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:41:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:41:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:41:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:41:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:41:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:41:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:41:02 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:41:02 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:41:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:41:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:41:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fda1bb6a32e3206e092d04e6f2b4989287f7414006a3c19fdd79101c7c0320`  
		Last Modified: Thu, 13 Nov 2025 23:28:34 GMT  
		Size: 1.5 MB (1450088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d628e848bfe7ecb94b3fa8754c2036aaf9a7ea4c754f9a7cb38d43ed8a694e2`  
		Last Modified: Fri, 14 Nov 2025 01:40:52 GMT  
		Size: 172.8 MB (172785530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba531f6a0d01db7e485725a868a6cbd85df2232696ef4b78209c60a7dc9d663`  
		Last Modified: Fri, 14 Nov 2025 01:41:18 GMT  
		Size: 3.1 MB (3113005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeaff5c0105bac867339b319ecade525bbee9b1ebe94a86b1f6eb0c3c22ac85`  
		Last Modified: Fri, 14 Nov 2025 01:41:19 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b0b5ebe82fcd0181526ce46f0a65a448f206c45016b699716184ba4cdf8f16`  
		Last Modified: Fri, 14 Nov 2025 01:41:18 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68dd45f01c340c39c62d3c0853149518dfe7d128f69dd987c80d716a255ced`  
		Last Modified: Fri, 14 Nov 2025 01:41:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:ea9077b11bf51ee5af9ca43eb4ff9d205676576e20a4aedd45c54328c6ac5a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90afcb95d4e6a9b1524e8ab5dd8a0aee8a05273698b95044bb4c40f5a9fb47b`

```dockerfile
```

-	Layers:
	-	`sha256:201358824bf7ca6f6716cd8f887e6467eba07260236d45d406476efa5c2fd336`  
		Last Modified: Fri, 14 Nov 2025 03:32:15 GMT  
		Size: 3.3 MB (3276870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3250297283951100e461103d6bbb1488d674a17a00bb9183141dfdf7327a5faf`  
		Last Modified: Fri, 14 Nov 2025 03:32:16 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:c6e75810859715a997612e5a19c17dd01d3d8756b35eb6e2fd047b31618fe55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223094720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a652f59a23ff30f69374a03fb882009c0fce1ba06cb7c4a6cfe528ed81c071`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:11:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:11:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 14 Nov 2025 14:32:12 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 14:32:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 14:32:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:32:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 14:32:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 14:32:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 14:32:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 14:32:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 14:32:14 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 14:32:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 14:32:14 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 14:32:14 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 14:32:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 14:32:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 14:32:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c6623dd21855ae1933ed5c3eda4d5180cd11ab6de8632ffb7cfe68b8b9498`  
		Last Modified: Fri, 14 Nov 2025 04:37:44 GMT  
		Size: 173.9 MB (173942768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317cf5fe34f34b69abf2774dcb201a9a31d5c0f6a02e4536dad9038eeb0dea36`  
		Last Modified: Fri, 14 Nov 2025 14:32:54 GMT  
		Size: 3.9 MB (3925224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7224a7e67a698150f247d3b1329c6cf2ba2a3bd2f0080208ba40dbfb8895f19`  
		Last Modified: Fri, 14 Nov 2025 14:32:54 GMT  
		Size: 9.2 MB (9242598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec77457a047a22e02b6f2fedad15ccc622858b4dc033d62d4551ba1d46a63f5`  
		Last Modified: Fri, 14 Nov 2025 14:32:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb08185b9f4b59de620a764993bf6127dae4ed697291b89c7351fc051ae0bb2`  
		Last Modified: Fri, 14 Nov 2025 14:32:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:7f431a7823f7f9ffa2b7a3f9ad2289a95348082c541ddc29000088e314b464c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa858c427ff33a26ef0f582b3dd08f93bd06ecb9fff625c56b29ade224ba0bf2`

```dockerfile
```

-	Layers:
	-	`sha256:c822ff5fd4f6cf60897e8329394ef99ec8c0d02dc9b6be5b72cc06a70d2789f8`  
		Last Modified: Fri, 14 Nov 2025 15:28:47 GMT  
		Size: 3.3 MB (3262981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9462014373ee869d1c29df502f75a6b96d582a0182e25a897d77202c8a1be3b0`  
		Last Modified: Fri, 14 Nov 2025 15:28:48 GMT  
		Size: 18.9 KB (18852 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:52b2da76d2909e681fa776877ce87f29fceefdc397c1d74092eec9ef9fec06a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205059420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e9f4aebae307228de8e6a4fb5b9325b7b7e0aabeb075b46e8194cc800f43f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 14 Nov 2025 02:31:09 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:31:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 02:31:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:31:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 02:31:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 02:31:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 02:31:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 02:31:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:31:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 02:31:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 02:31:09 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 02:31:09 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 02:31:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 02:31:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 02:31:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f435bb0c415b0011e7ce572f4aace1b1bf6baf2e55cffcd5f380b640cd57b19a`  
		Last Modified: Fri, 14 Nov 2025 04:38:17 GMT  
		Size: 163.3 MB (163302983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2685b4dd6ef894449c5ef418b7acb27c72f1559216fb35f4a0c6ac03bee3da1`  
		Last Modified: Fri, 14 Nov 2025 02:31:29 GMT  
		Size: 3.1 MB (3053769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03143804599bf7d99bb7165dc61a3ff0ccd9a8ff1f954da0dab5efe4093a50c`  
		Last Modified: Fri, 14 Nov 2025 02:31:31 GMT  
		Size: 9.2 MB (9242580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685990eeeaef3c6bee8edd4e2f5b754c27c76d18ce8b19550648ceaa9d7ca8f8`  
		Last Modified: Fri, 14 Nov 2025 02:31:29 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f429434524c8a2cc11676ed7d977b5903c16dabdd34c53faf3fe683e2f85a3b9`  
		Last Modified: Fri, 14 Nov 2025 02:31:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:57660fe0872d70c0e83637b2038c28a55082a6931f2acb42b9225a7d16e517fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ba15971a246003c17c87933321bc009e395012413007a762a13f5c42df3257`

```dockerfile
```

-	Layers:
	-	`sha256:cf195217b568f462475682dbe545c2272841f53adc71ae1e42db839fa081acfe`  
		Last Modified: Fri, 14 Nov 2025 03:32:23 GMT  
		Size: 3.0 MB (2950170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef92f0033d0bb64a17f2f75cd07ff907b29653f1bc5b61a393bb274bec5b17a`  
		Last Modified: Fri, 14 Nov 2025 03:32:24 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json
