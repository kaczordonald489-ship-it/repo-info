<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.6`](#silverpeas636)
-	[`silverpeas:6.4.4`](#silverpeas644)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.6`

```console
$ docker pull silverpeas@sha256:33ed0f75873506bc58e6a892334d0eb85d8ce981b5200feefb91c21931dd5cb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:1b414180c805953a70438ae7192efe28a4646aabd7d7d617a5ba2b4adce995db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1887122515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1a84495cd5be29fe53fdb9f4b1b2a16316191f574c3b9c0c9f156727f983cf`
-	Default Command: `["\/opt\/run.sh"]`

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
# Thu, 13 Nov 2025 23:42:38 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 13 Nov 2025 23:42:38 GMT
ENV TERM=xterm
# Thu, 13 Nov 2025 23:42:38 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 13 Nov 2025 23:42:40 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 13 Nov 2025 23:42:43 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 13 Nov 2025 23:42:43 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 13 Nov 2025 23:43:06 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 13 Nov 2025 23:43:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:43:06 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 13 Nov 2025 23:43:06 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:43:06 GMT
ENV PING_ON=1
# Thu, 13 Nov 2025 23:43:07 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 13 Nov 2025 23:43:07 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 13 Nov 2025 23:43:07 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 13 Nov 2025 23:43:07 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 13 Nov 2025 23:43:07 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 13 Nov 2025 23:43:07 GMT
ENV SILVERPEAS_VERSION=6.3.6
# Thu, 13 Nov 2025 23:43:07 GMT
ENV WILDFLY_VERSION=26.1.1
# Thu, 13 Nov 2025 23:43:07 GMT
LABEL name=Silverpeas 6.3.6 description=Image to install and to run Silverpeas 6.3.6 vendor=Silverpeas version=6.3.6 build=2
# Thu, 13 Nov 2025 23:43:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 13 Nov 2025 23:43:25 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 13 Nov 2025 23:43:25 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 13 Nov 2025 23:43:25 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 13 Nov 2025 23:43:25 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 13 Nov 2025 23:43:25 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 13 Nov 2025 23:44:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Thu, 13 Nov 2025 23:44:56 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 13 Nov 2025 23:44:56 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 13 Nov 2025 23:44:56 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d206039f988c38bc80cdbb4a00c50b5d18f6dd7464dd9318e2f659ae6b2b20`  
		Last Modified: Fri, 14 Nov 2025 18:10:26 GMT  
		Size: 871.4 MB (871445359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e0ee028d7f67bc4c2ea14a897b85b781598ac1492b170238b3e4bb53636b7c`  
		Last Modified: Thu, 13 Nov 2025 23:47:46 GMT  
		Size: 4.0 MB (3994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e7977abcb2c8cc94c60fde2d558e55271578f12aed057095ab27445286fd3f`  
		Last Modified: Thu, 13 Nov 2025 23:47:46 GMT  
		Size: 7.1 MB (7146615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269b837ac96a41ee7845ade70a376f225d3c477a24ebe5911c51c14feecd21c1`  
		Last Modified: Thu, 13 Nov 2025 23:47:46 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b242b3de5ba6d3882d624d0aa629decbd7b209c9d094441340a93bcf88d88f`  
		Last Modified: Thu, 13 Nov 2025 23:47:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed5a25d42e93601c47a88045bb9aa6b683ecaa4fdeda2405c0873c57b43fbc`  
		Last Modified: Thu, 13 Nov 2025 23:47:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d907f43fd89465e74e32fea37a2e061086fbd04e4c27bade7363cf0913c73742`  
		Last Modified: Fri, 14 Nov 2025 18:10:21 GMT  
		Size: 217.8 MB (217843269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fece708e9a640de291a69f6385b27eca7b1391e6316f72f46d10deca39b581a8`  
		Last Modified: Thu, 13 Nov 2025 23:47:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3fadac2ac7a4680491442b769545e4c4e7f7b33f0d199a4ef422e3921538af`  
		Last Modified: Thu, 13 Nov 2025 23:47:45 GMT  
		Size: 665.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0e53546bae4fd790cd70384294f2ec6edb22ed5cbd4653916de63f1ddf23f5`  
		Last Modified: Thu, 13 Nov 2025 23:47:45 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef46ec56e510229f6cfd78fe3799ebbae641f940fb81b7ac34d991a4ff7806d1`  
		Last Modified: Thu, 13 Nov 2025 23:47:46 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fc52f720ecb837e8d8391192583f1e9be567be3e8460e4844ab520162ffadb`  
		Last Modified: Fri, 14 Nov 2025 18:10:47 GMT  
		Size: 754.6 MB (754615078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:7e68dc26d64541b4c3a809f8c4decbf3cdd9a560446fb079f28b6bc3da1b06b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26866180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84480fadba72992538aac7ca7bb1326b1f1681ef36a7dbfeef62074617d7ee3`

```dockerfile
```

-	Layers:
	-	`sha256:838ef06d37a0743c390e537a7453c736aa33cf939bea2ef35d89405d17c2a322`  
		Last Modified: Fri, 14 Nov 2025 02:09:33 GMT  
		Size: 26.8 MB (26825478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16e917f53d006fb3ad95296ab52549a827883f12c7827ddf66a83cc0597f82a`  
		Last Modified: Fri, 14 Nov 2025 02:09:34 GMT  
		Size: 40.7 KB (40702 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.4`

```console
$ docker pull silverpeas@sha256:cf6de919f66f028bff62d965329bc68aefcd70cb0f74f455032995c96ce2d3ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.4` - linux; amd64

```console
$ docker pull silverpeas@sha256:ff2f47bab7bcebb5f9d890ba7ecb51b0b2adc7ea2188ede4865821e18867b961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817985432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d46af11415490d691f370a6c6db970dcb6f9b6791d731f51727f091d42df4`
-	Default Command: `["\/opt\/run.sh"]`

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
# Thu, 13 Nov 2025 23:41:50 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 13 Nov 2025 23:41:50 GMT
ENV TERM=xterm
# Thu, 13 Nov 2025 23:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 13 Nov 2025 23:41:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 13 Nov 2025 23:41:54 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 13 Nov 2025 23:41:54 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 13 Nov 2025 23:42:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
ENV PING_ON=1
# Thu, 13 Nov 2025 23:42:17 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 13 Nov 2025 23:42:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 13 Nov 2025 23:42:18 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 13 Nov 2025 23:42:18 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 13 Nov 2025 23:42:18 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 13 Nov 2025 23:42:18 GMT
ENV SILVERPEAS_VERSION=6.4.4
# Thu, 13 Nov 2025 23:42:18 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 13 Nov 2025 23:42:18 GMT
LABEL name=Silverpeas 6.4.4 description=Image to install and to run Silverpeas 6.4.4 vendor=Silverpeas version=6.4.4 build=1
# Thu, 13 Nov 2025 23:42:41 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 13 Nov 2025 23:44:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 13 Nov 2025 23:44:22 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 13 Nov 2025 23:44:22 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 13 Nov 2025 23:44:22 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a99586bfe1f608daba9b93c4e9e3d157801ba0fbb4fb18a3c5a00d581169a`  
		Last Modified: Fri, 14 Nov 2025 10:40:07 GMT  
		Size: 494.8 MB (494795738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5339f6f6a67ad2e3c907a7657906a6ca7823451ca77309d96482ef9fc5cbf03f`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 4.0 MB (3994005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4436454fd3e00d4b5b2f5380f68fdbc8d6c36cad1c69842ad731335b2b916e52`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 7.1 MB (7146601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af47471684cf16323a210ded3b4a3fd620769e1e96da3e54d492fe6adcc77c`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 2.5 MB (2538617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a4a19f2609266ad7dbdf636dd9085b88e57b8379e5327071f5bc50a9eb64f`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf5648edfb328190e60eec678de44d1898d64fa628bff234f662bf9b94e2ca`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879bb4405f9465ee5c76fd2054de43ac0b67b1042ac78c1b1cc78776089208bf`  
		Last Modified: Fri, 14 Nov 2025 10:40:19 GMT  
		Size: 269.1 MB (269106248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aab84240c9a6a675d7f94d022f07d503f1c79e2b4a718493e9fdbd17833eb6`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2833553916d40f30b57ee7f7a50b17266a2c7e6bc1b883368d1977fa508295`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3480cc1620037405505173a742ef341dc7d8fc658c7ae51dd73b666154642b1`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bea7469ace72f8106e811ff64d684dee2bdfde161a24cb0c922e59154f1020`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83287ef6ed8b305a3f323126852df3a4d565f4acfa6436755d4dbce5e0d013`  
		Last Modified: Fri, 14 Nov 2025 10:40:56 GMT  
		Size: 1.0 GB (1010864126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.4` - unknown; unknown

```console
$ docker pull silverpeas@sha256:a045a57a93213e7194eaa9c79efbd04282f700aa3e2cbae29d2f7340b135bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d86ceafa806bd1b5480474fe0ce1410fc0f37c8f4545c70085a7806a4fd00d`

```dockerfile
```

-	Layers:
	-	`sha256:8404e48033a6f06fe5c79677afec76a9de88ddf332a6cfb697739ea8632f4ece`  
		Last Modified: Fri, 14 Nov 2025 02:09:39 GMT  
		Size: 16.6 MB (16605649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3728f815d43463c3db62afb52f1bbffecd398dc78f5b6687b67fd06232ac74a`  
		Last Modified: Fri, 14 Nov 2025 02:09:40 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:cf6de919f66f028bff62d965329bc68aefcd70cb0f74f455032995c96ce2d3ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:ff2f47bab7bcebb5f9d890ba7ecb51b0b2adc7ea2188ede4865821e18867b961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817985432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d46af11415490d691f370a6c6db970dcb6f9b6791d731f51727f091d42df4`
-	Default Command: `["\/opt\/run.sh"]`

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
# Thu, 13 Nov 2025 23:41:50 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 13 Nov 2025 23:41:50 GMT
ENV TERM=xterm
# Thu, 13 Nov 2025 23:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 13 Nov 2025 23:41:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 13 Nov 2025 23:41:54 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 13 Nov 2025 23:41:54 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 13 Nov 2025 23:42:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:42:17 GMT
ENV PING_ON=1
# Thu, 13 Nov 2025 23:42:17 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 13 Nov 2025 23:42:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 13 Nov 2025 23:42:18 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 13 Nov 2025 23:42:18 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 13 Nov 2025 23:42:18 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 13 Nov 2025 23:42:18 GMT
ENV SILVERPEAS_VERSION=6.4.4
# Thu, 13 Nov 2025 23:42:18 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 13 Nov 2025 23:42:18 GMT
LABEL name=Silverpeas 6.4.4 description=Image to install and to run Silverpeas 6.4.4 vendor=Silverpeas version=6.4.4 build=1
# Thu, 13 Nov 2025 23:42:41 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 13 Nov 2025 23:42:41 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 13 Nov 2025 23:44:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 13 Nov 2025 23:44:22 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 13 Nov 2025 23:44:22 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 13 Nov 2025 23:44:22 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a99586bfe1f608daba9b93c4e9e3d157801ba0fbb4fb18a3c5a00d581169a`  
		Last Modified: Fri, 14 Nov 2025 10:40:07 GMT  
		Size: 494.8 MB (494795738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5339f6f6a67ad2e3c907a7657906a6ca7823451ca77309d96482ef9fc5cbf03f`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 4.0 MB (3994005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4436454fd3e00d4b5b2f5380f68fdbc8d6c36cad1c69842ad731335b2b916e52`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 7.1 MB (7146601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63af47471684cf16323a210ded3b4a3fd620769e1e96da3e54d492fe6adcc77c`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 2.5 MB (2538617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a4a19f2609266ad7dbdf636dd9085b88e57b8379e5327071f5bc50a9eb64f`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf5648edfb328190e60eec678de44d1898d64fa628bff234f662bf9b94e2ca`  
		Last Modified: Thu, 13 Nov 2025 23:46:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879bb4405f9465ee5c76fd2054de43ac0b67b1042ac78c1b1cc78776089208bf`  
		Last Modified: Fri, 14 Nov 2025 10:40:19 GMT  
		Size: 269.1 MB (269106248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aab84240c9a6a675d7f94d022f07d503f1c79e2b4a718493e9fdbd17833eb6`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2833553916d40f30b57ee7f7a50b17266a2c7e6bc1b883368d1977fa508295`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3480cc1620037405505173a742ef341dc7d8fc658c7ae51dd73b666154642b1`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bea7469ace72f8106e811ff64d684dee2bdfde161a24cb0c922e59154f1020`  
		Last Modified: Thu, 13 Nov 2025 23:46:30 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83287ef6ed8b305a3f323126852df3a4d565f4acfa6436755d4dbce5e0d013`  
		Last Modified: Fri, 14 Nov 2025 10:40:56 GMT  
		Size: 1.0 GB (1010864126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:a045a57a93213e7194eaa9c79efbd04282f700aa3e2cbae29d2f7340b135bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d86ceafa806bd1b5480474fe0ce1410fc0f37c8f4545c70085a7806a4fd00d`

```dockerfile
```

-	Layers:
	-	`sha256:8404e48033a6f06fe5c79677afec76a9de88ddf332a6cfb697739ea8632f4ece`  
		Last Modified: Fri, 14 Nov 2025 02:09:39 GMT  
		Size: 16.6 MB (16605649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3728f815d43463c3db62afb52f1bbffecd398dc78f5b6687b67fd06232ac74a`  
		Last Modified: Fri, 14 Nov 2025 02:09:40 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json
