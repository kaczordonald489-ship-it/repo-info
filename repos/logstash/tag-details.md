<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.18.8`](#logstash8188)
-	[`logstash:8.19.7`](#logstash8197)
-	[`logstash:9.1.7`](#logstash917)
-	[`logstash:9.2.1`](#logstash921)

## `logstash:8.18.8`

```console
$ docker pull logstash@sha256:f2608dcb12d14d3aa4a3aad470bbcac1f5cc391baa64a0c560f41a70c7e514b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.8` - linux; amd64

```console
$ docker pull logstash@sha256:0c561a809266e5787e59e27cf7c10ad53a51d695aa01464b3fe1fe3447f28303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.8 MB (525824723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2d032d949a350fca05beb8a66e8387d7e95d55153b47169c374c5c5c97d650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 13 Nov 2025 23:28:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:56 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:37 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:37 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:37 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:37 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:38 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Thu, 13 Nov 2025 23:29:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd79b80ccaa55c41f750c02665aedad9405ced41da54b49d0be9208fd2d5d6`  
		Last Modified: Thu, 13 Nov 2025 23:30:45 GMT  
		Size: 49.0 MB (49030452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429834f6c7f98c2abc9f1c4742c85442daf5653762f7a26de93eb462bac346df`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1e8a17be130a7f1d7217bdb655fd8126de4f651453d3d6e89436d6d1d342b0`  
		Last Modified: Fri, 14 Nov 2025 02:26:54 GMT  
		Size: 441.0 MB (440981473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d1fa58ef233269bc32839e4f818d021168cb0c6e80e0200148f4c3cff15b0f`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30fbcc4fda19e49a762266e0e6faded74b019c5aabdb92f222341949c77a44c`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20a0b4ac67d42cb574f5eb946d234c5257b40c6b153f029dc385f75f6a8ce2a`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c249e208f213784ac2ece9cea2b943c597c3cf702e90c5f37cb445217ed81`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb233dac8d41e821577474435b7f1a1769b4bee17a2e45734d903c3eb6bcf0c`  
		Last Modified: Thu, 13 Nov 2025 23:30:41 GMT  
		Size: 4.0 MB (4004180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a382d3f5355e9be2f82d6625b36b3a8e72685cfcf41b1b116ca460e6b39b4efe`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 2.1 MB (2078022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664a3632afa8063325511c3e4f4995f36e06390039e1a84893ebdd91e574e018`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:2b0556efd6d5028087e0dcb7eaf140ae64c164864695dd5a4180bb4eb6872d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ace81df77812ed20bb2a9d7277e0e88c0e1c9da9ee07e7bf541d544ece1077f`

```dockerfile
```

-	Layers:
	-	`sha256:e9a099deaf531ca02082a6f0b37812c340b9e4419acc44f046dcd834a9c26c2c`  
		Last Modified: Fri, 14 Nov 2025 01:53:26 GMT  
		Size: 3.7 MB (3657663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d73e810d46eba1a1728c1b8064af55f67a3a2dc44d3da8cf9c8664068be48f`  
		Last Modified: Fri, 14 Nov 2025 01:53:26 GMT  
		Size: 34.6 KB (34608 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:eda3d8c0f02db1a48df7826ed5a096b0c5331594e5a6f67397e8c5a9614cc57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.0 MB (524967182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b14e7870f762fbe697e10861bb87bb433bb4d7176d2ea76762c64a6d2ad8fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 13 Nov 2025 23:28:31 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:14 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:14 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Thu, 13 Nov 2025 23:29:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e2941a2ca4b19bbd5b2b6121b4d7ea76e18d66621a65bc2b69892a6695274a`  
		Last Modified: Thu, 13 Nov 2025 23:30:10 GMT  
		Size: 50.9 MB (50920587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92811a7a0282e3c3ac478c27030a0833d205ecfa3722d637ff310259ff4c61cd`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46880e8efe89d131f1fcef7fbbc1bac25b066a52c522510ea5a4d54905c43408`  
		Last Modified: Fri, 14 Nov 2025 02:27:30 GMT  
		Size: 439.2 MB (439248985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e816dbf151b745cf877898cf1f38eb5d1e9fdba9cb829677c7db3f51e2356a`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd8b3a2856c46ef6c5fc08409f79704e1e152daf357e774a4112e9a0e6e3310`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38a53e225d75eff12773ef054757fc3c918925e9c6a254255a6abae89b9454d`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0611631f79d04d18e50936612a7f2ed8941206427eb741095e883b9554d5abd9`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1c7deb1dda72ff0ea0be3b4ec4a75470d63cdc3b774dbbed0ce150ef7c8aa6`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 4.0 MB (4004181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769e7b7e10a84cb8c18514c4fb229e6085c41326be9344426201b72d03d95cb`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.9 MB (1925573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7261f1bc119d985222300eb703ac17b3f85ef3be1d2b7c59548d52b1931610`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:282ec9c8c443d33ce1d7b8ae801910caf07e84f50e12b7640d560cce877f10f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc02dbb43679cc9148cb7874de46881ffa09231366dd245364e0924316feaec`

```dockerfile
```

-	Layers:
	-	`sha256:eb2724933da0910479dfd0de4d69f32aaede2048f786924e0754d75f1a82048a`  
		Last Modified: Fri, 14 Nov 2025 01:53:31 GMT  
		Size: 3.7 MB (3658088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff2be8520e57438521bdce72e162db54d896d0333fd5b8b4a3e65312794eb7f`  
		Last Modified: Fri, 14 Nov 2025 01:53:32 GMT  
		Size: 34.8 KB (34752 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.7`

```console
$ docker pull logstash@sha256:49df884c1068983a34af7bc31a1f81ab4279bcffbab698e201e8a46a7210590b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.7` - linux; amd64

```console
$ docker pull logstash@sha256:2a4b36a326068588554f600a96d0a98ab9c26b88ec0273024dd103af9bc69ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.2 MB (526243157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594605f93ea9784545a63eeb0cdd575f7af3fa5ab56f9a388ae431b1387a043`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 13 Nov 2025 23:28:58 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:59 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:38 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:38 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:39 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.7 org.opencontainers.image.version=8.19.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-04T18:31:44+00:00 org.opencontainers.image.created=2025-11-04T18:31:44+00:00
# Thu, 13 Nov 2025 23:29:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff90193b95fb19e4f476b7f04f879023aa7c2919ba3dbd305c392fe481909c72`  
		Last Modified: Thu, 13 Nov 2025 23:30:33 GMT  
		Size: 49.0 MB (49030468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cf3e8735f7211d5096f908fa83e51cd1283a8715e80083851ee811d3c6ab2e`  
		Last Modified: Thu, 13 Nov 2025 23:30:30 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94c12b7ce0c034d668bd970d5f5164af02046f0c709ef756177cb8dd8d94a6c`  
		Last Modified: Fri, 14 Nov 2025 02:25:29 GMT  
		Size: 441.4 MB (441397950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adf37063a9f4db09ab05e0a7cf30465972ac6d8ef629ccc468ed40052904071`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf601524a146f2507b8e6dcd31b1220232b3948401f0a8b9598e6d1bce5fe22`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f820cd3ad32d9b3d8de95154da1b33fb379dedc14494161e28cfa1038c5aa65`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09044aedf3a8739fe029075c3b8230d4ec51d6a9400eecfd4b7d8ed4678ba4`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f53632abd983b209fe839ae0cbc458dcc2b6b55c7b7fd2c6c1ee39e2d248dcb`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 4.0 MB (4005469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b380f3267c3a88eebbca8078dcd80bb0a086ac8bf7bce7516c0523b479c03f36`  
		Last Modified: Thu, 13 Nov 2025 23:30:30 GMT  
		Size: 2.1 MB (2078666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd43b587ce39783a1027a5ddefc25df9d6f4df10730e7b43644e2e5ed7aba6`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.7` - unknown; unknown

```console
$ docker pull logstash@sha256:168a2252d7fcc9f127368442cabef6cf601d17ddac28c7d7960ba8f9956904b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d1bd1576defe445eb6e8d35307fb9558b8b8a55e819c1d7960b9bdfb76131d`

```dockerfile
```

-	Layers:
	-	`sha256:4fb9fe7e9fd44457c7a082d6d8bd10b79a988bc4aaaca5843e08f7c079161c48`  
		Last Modified: Fri, 14 Nov 2025 01:53:35 GMT  
		Size: 3.7 MB (3653221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b531694c6f7ad13f3f30cdb1638f9564f42d493b791b3e606b6447d01235b4f6`  
		Last Modified: Fri, 14 Nov 2025 01:53:35 GMT  
		Size: 34.6 KB (34612 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:687d30ee863290f416a9344f434a7f425d80a6262c107ccb9a4b6c43f05b451c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525403370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf30ad8c23d7acbc32d92043eb98675b6bceaa3675696aad583e5eb1e593a1f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 13 Nov 2025 23:28:30 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.7 org.opencontainers.image.version=8.19.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-04T18:31:44+00:00 org.opencontainers.image.created=2025-11-04T18:31:44+00:00
# Thu, 13 Nov 2025 23:29:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed524d9de1f203d2c1af7057d298666cbd488f2248ae06c4997f2665808977cc`  
		Last Modified: Thu, 13 Nov 2025 23:30:12 GMT  
		Size: 50.9 MB (50920543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b599cedf77b61925226d81a77267d2176a938ffadb159c7c298bbff0ab33cb30`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf5a448feb9d96d06df1bcb8773b364693b852aa24dbdfeb376b02a6e399b7`  
		Last Modified: Fri, 14 Nov 2025 02:26:04 GMT  
		Size: 439.7 MB (439682989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111c29a4877e9b1d21de678530eb31664b44c2ebfe17cb480d962118ce008265`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796c9e12c13eec50fbd5ba636a5378f96c057ed6f4ff6b4e4e972e140d975336`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21e87a7961528613dbf0c07c91f0da0ffc963cff13c2b49d8ca47eccdca267`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df883f3589cfa4fce086242bb1b8ba33014436661a49a599ebc593a9fe66c9e8`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16b66a44c5ac0a3c21e84e9d3c3641f3c6f49ef08b43d4f1d03ea63b64c28b`  
		Last Modified: Thu, 13 Nov 2025 23:30:08 GMT  
		Size: 4.0 MB (4005469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1712271c13bd779319b6dcf8eb07e84bd3452dd7950d3f3fa0917a0a7efdc1f`  
		Last Modified: Thu, 13 Nov 2025 23:30:08 GMT  
		Size: 1.9 MB (1926505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88216873916a581231d01ffd74c4b05124cb4fc7e8b3d8603481a4e38a984e48`  
		Last Modified: Thu, 13 Nov 2025 23:30:08 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.7` - unknown; unknown

```console
$ docker pull logstash@sha256:b5cd6760869587fcceda70901f12dcb45e1ec7e08979a57b7e25ee82acee470d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2463afd5d871f2363ee7206f2fa0b1242c912783bd2a5349bcb378c82f79b82`

```dockerfile
```

-	Layers:
	-	`sha256:e28a155d2bf8744e624f1814393eaf01f4a7770d594eddf53b1833ef42848d0c`  
		Last Modified: Fri, 14 Nov 2025 01:53:40 GMT  
		Size: 3.7 MB (3653646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7006e0acbb5095a9edbf1ad412390e64481791be5029909383227f80b8a62257`  
		Last Modified: Fri, 14 Nov 2025 01:53:41 GMT  
		Size: 34.8 KB (34756 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.7`

```console
$ docker pull logstash@sha256:c1bd4d54d74405f34ed46aef245ca6d47ecd1b08b9c60a01596afc5bd05742eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.7` - linux; amd64

```console
$ docker pull logstash@sha256:e01645982b6ddfe7bf8f4ecef9d0f320bc50222cadfca4cdaecfcc7edc33302f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.5 MB (477545972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6c2277efca1f25af14dff04de4ba092831c0f211b31989485d1a321f91eebb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:51:18 GMT
ENV container oci
# Mon, 17 Nov 2025 06:51:19 GMT
COPY dir:7cf80e1c5cade8bdab1a4d70632d27e8826f968a3bd11979550b2850547e929b in /      
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:51:19 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:51:01Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Tue, 18 Nov 2025 11:17:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 18 Nov 2025 11:17:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 11:17:14 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 11:17:14 GMT
WORKDIR /usr/share
# Tue, 18 Nov 2025 11:17:21 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 18 Nov 2025 11:17:52 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 18 Nov 2025 11:17:52 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 18 Nov 2025 11:17:52 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 18 Nov 2025 11:17:52 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 18 Nov 2025 11:17:52 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 18 Nov 2025 11:17:52 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 11:17:52 GMT
WORKDIR /usr/share/logstash
# Tue, 18 Nov 2025 11:17:52 GMT
USER 1000
# Tue, 18 Nov 2025 11:17:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 18 Nov 2025 11:17:52 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 18 Nov 2025 11:17:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba9d6a51bacc7fbae40184a0fc70408041158c4c67c48a095938163240f47ce`  
		Last Modified: Tue, 18 Nov 2025 11:18:45 GMT  
		Size: 5.2 MB (5156424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baff5138393b4c6e80b1ffe39168965774317d66fc8636b601a15e357eef936c`  
		Last Modified: Tue, 18 Nov 2025 15:35:12 GMT  
		Size: 430.3 MB (430328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec3e8a376e8b616f3c1e92a912eeba1fb0c95cae26c025e6ede55d8521ed686`  
		Last Modified: Tue, 18 Nov 2025 11:18:45 GMT  
		Size: 2.1 MB (2078842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b1ad11d82ba05ff5366ef5b7f3cceb8ee1edfb7b5b5c2bd98b7a668463bed5`  
		Last Modified: Tue, 18 Nov 2025 11:18:45 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fad648884b1c7046096f3ae7ac684bf7fc2f172d2ddbb2a9df726231739e3b`  
		Last Modified: Tue, 18 Nov 2025 11:18:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27587b1d81241d7a172673aaf2be2f3e5b8664207509128c4e85e349137ddff2`  
		Last Modified: Tue, 18 Nov 2025 11:18:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad84d38bd76f529d178d92ca0fe72084d8e68eea5d4ef48f8d0c1e891bff25e9`  
		Last Modified: Tue, 18 Nov 2025 11:18:45 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:ecf89160b0ea3a5ff402826b43cdc22594b2262c361a4b2f57adb2a4bd3a8d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f464d6a2f7db6b81940b7909b99b95365043af4bda96831909b40b792dce0a2e`

```dockerfile
```

-	Layers:
	-	`sha256:043eaf0e2f5a67566f8e7e6542b36495dd62c6d2ffd636cec3d208f67ff097ab`  
		Last Modified: Tue, 18 Nov 2025 16:54:46 GMT  
		Size: 2.1 MB (2090558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d662f87d689fa17e14a0aba33567c3599005fe80a1960fa10dbf92d673f272f1`  
		Last Modified: Tue, 18 Nov 2025 16:54:47 GMT  
		Size: 29.6 KB (29554 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:556c6e34af54788ccc0a6f5ef7d86af0fd1b86114351c9533f0beda9d5cf83b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.9 MB (473888701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f07c51a7736c0303aa83bf644cbd4ee4f37d4c347e5a6939ece737f12a3a914`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:55:56 GMT
ENV container oci
# Mon, 17 Nov 2025 06:55:57 GMT
COPY dir:87932faf9829020ce186f9ca70767f10cf2708680f90badc643a8b214cc3a6f7 in /      
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:55:57 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:55:41Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Tue, 18 Nov 2025 07:23:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 18 Nov 2025 07:23:22 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:23:22 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 07:23:22 GMT
WORKDIR /usr/share
# Tue, 18 Nov 2025 07:23:30 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 18 Nov 2025 07:24:23 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 18 Nov 2025 07:24:24 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 18 Nov 2025 07:24:24 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 18 Nov 2025 07:24:24 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 18 Nov 2025 07:24:24 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 18 Nov 2025 07:24:24 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:24:24 GMT
WORKDIR /usr/share/logstash
# Tue, 18 Nov 2025 07:24:24 GMT
USER 1000
# Tue, 18 Nov 2025 07:24:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 18 Nov 2025 07:24:24 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 18 Nov 2025 07:24:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f5fa84ab80aa66e0c9cc6b95c1cb73db52b3783ab92aeea0eaab98235b7db3`  
		Last Modified: Tue, 18 Nov 2025 07:25:18 GMT  
		Size: 5.2 MB (5156703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2137d628f7d9d5ab37deef382a419bcc42eb7abed126908d71c085f7e0ea190`  
		Last Modified: Tue, 18 Nov 2025 20:25:31 GMT  
		Size: 428.6 MB (428601936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc2cbfd9628fb28481d310c35028edd1248b22e8bd3d78c6ffc59ce993bc075`  
		Last Modified: Tue, 18 Nov 2025 07:25:18 GMT  
		Size: 1.9 MB (1926864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c8e10764c6e5c0675108a1b2b4134f2e4971bbe2028bce188a41e4f3c5157`  
		Last Modified: Tue, 18 Nov 2025 07:25:18 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce36fedf03d9de52c5416e44bad069656f9569cbc6c63fd6e5fa336a20fa5e0`  
		Last Modified: Tue, 18 Nov 2025 07:25:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3567a9e70aff4b3b1d3a8bc03731dd18a4f8b92c9892d697d5da8e8c66968f3`  
		Last Modified: Tue, 18 Nov 2025 07:25:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8dbe9ec65012d9d1f38a48b480796a89c5788020c8660fa201f8fcfe41bc0`  
		Last Modified: Tue, 18 Nov 2025 07:25:18 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:a9b7d9cea41c2c57935dd4d3e09cf03fb5d5ea56ecd567e81429a99422f5c8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bc61147502917ab9830ef2036bcc789a53c8c73eda9d1a152f3ba1cad7078a`

```dockerfile
```

-	Layers:
	-	`sha256:5d50abff881da25eaea7bdc0a36efe477857a24c41c3cdd7e80661f5b949f0fe`  
		Last Modified: Tue, 18 Nov 2025 10:54:23 GMT  
		Size: 2.1 MB (2091128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b734b18930dce2eba007269ad9e7318e434f0a8b71d349d8f81ea05aadc98a9`  
		Last Modified: Tue, 18 Nov 2025 10:54:24 GMT  
		Size: 29.7 KB (29671 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.1`

```console
$ docker pull logstash@sha256:2e16ca4354a460987ce1e0bcb46401e53680a19b5b3de529c0bfabee70107096
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.1` - linux; amd64

```console
$ docker pull logstash@sha256:0f09f487130165e8b811447fe9a0329eddf8ee67727df8e7bfa56f6c86641a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.8 MB (487848280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f912b291d0dad19b53997defe9bf2ceda107f2301a8c9e16e33c0d772720e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:51:18 GMT
ENV container oci
# Mon, 17 Nov 2025 06:51:19 GMT
COPY dir:7cf80e1c5cade8bdab1a4d70632d27e8826f968a3bd11979550b2850547e929b in /      
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:51:19 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:51:01Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Tue, 18 Nov 2025 11:17:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 18 Nov 2025 11:17:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 11:17:14 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 11:17:14 GMT
WORKDIR /usr/share
# Tue, 18 Nov 2025 11:17:21 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 18 Nov 2025 11:19:38 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 18 Nov 2025 11:19:38 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 18 Nov 2025 11:19:38 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 18 Nov 2025 11:19:38 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 18 Nov 2025 11:19:38 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 18 Nov 2025 11:19:38 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 11:19:39 GMT
WORKDIR /usr/share/logstash
# Tue, 18 Nov 2025 11:19:39 GMT
USER 1000
# Tue, 18 Nov 2025 11:19:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 18 Nov 2025 11:19:39 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 18 Nov 2025 11:19:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba9d6a51bacc7fbae40184a0fc70408041158c4c67c48a095938163240f47ce`  
		Last Modified: Tue, 18 Nov 2025 11:18:45 GMT  
		Size: 5.2 MB (5156424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58287dae960d9fa0ba561b3693aff548c440cf7c6b95645e6a52c5f9c895633d`  
		Last Modified: Tue, 18 Nov 2025 17:05:58 GMT  
		Size: 440.6 MB (440630651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586cfdc959eb4d5021ffadcfefe8b057f77cb723a70f0f0734afa00dd991b769`  
		Last Modified: Tue, 18 Nov 2025 11:20:28 GMT  
		Size: 2.1 MB (2078837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f283d82b3ce8eb2a8eb1adec4678ee35c62f1332ee53638485894499074963e5`  
		Last Modified: Tue, 18 Nov 2025 11:20:28 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8af94f38318230aa561fb2e179128194ab86779738fdceb6b3059ab4253817`  
		Last Modified: Tue, 18 Nov 2025 11:20:28 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cbc4cf3c91ec6aa949cb6ff87359826e6d3cd0019032fb1ac99035a11b6ee5`  
		Last Modified: Tue, 18 Nov 2025 11:20:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082e27ac4b6128cb1d5cefa7e126a7fd597fe0c27bef873a1676b728458af16c`  
		Last Modified: Tue, 18 Nov 2025 11:20:28 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:7b4a93e0e07723bc2c0209d0d7135ea7b19dd28d9a29a68326dbff006f8ad86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a5dbb7ea1462bc12f75110937efbb8d993b1c47a2b0bb1cb154567514bed79`

```dockerfile
```

-	Layers:
	-	`sha256:616cff83c5ed50805fa656cf22cfdf5ba550e27b22ef111817151a73488f9b92`  
		Last Modified: Tue, 18 Nov 2025 16:54:43 GMT  
		Size: 2.1 MB (2100378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57707631ecf19241c54b208bb5a07764317daf71183cf1673fc54d3ee0888f9d`  
		Last Modified: Tue, 18 Nov 2025 16:54:44 GMT  
		Size: 29.6 KB (29602 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:32e2858600f44082c3069c3310e54934e94efd06a7a39ceaaaa62fbe818b7130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.2 MB (484191805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e507c1fa36790fdd13c7f3aeabd7666028852d03742ed510f35d45b1b57b45`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:55:56 GMT
ENV container oci
# Mon, 17 Nov 2025 06:55:57 GMT
COPY dir:87932faf9829020ce186f9ca70767f10cf2708680f90badc643a8b214cc3a6f7 in /      
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:55:57 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:55:41Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Tue, 18 Nov 2025 07:25:44 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 18 Nov 2025 07:25:44 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:25:44 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 07:25:44 GMT
WORKDIR /usr/share
# Tue, 18 Nov 2025 07:25:47 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 18 Nov 2025 07:26:07 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 18 Nov 2025 07:26:07 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 18 Nov 2025 07:26:07 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 18 Nov 2025 07:26:07 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 18 Nov 2025 07:26:07 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 18 Nov 2025 07:26:07 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 07:26:07 GMT
WORKDIR /usr/share/logstash
# Tue, 18 Nov 2025 07:26:07 GMT
USER 1000
# Tue, 18 Nov 2025 07:26:07 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 18 Nov 2025 07:26:07 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 18 Nov 2025 07:26:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8c4dfa7ac5427b7679b7937ce075d3b45e910e11121f6914879cda923a6a98`  
		Last Modified: Tue, 18 Nov 2025 07:26:57 GMT  
		Size: 5.2 MB (5156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0aa7cb803099c275f67d911902650d9f0f6f41b106837858ba9c57787d6111`  
		Last Modified: Tue, 18 Nov 2025 11:02:25 GMT  
		Size: 438.9 MB (438905108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc645f5f8c44696a089b12ff0871e1493a4f0c0f26497cf869204fe3cb2c4e7`  
		Last Modified: Tue, 18 Nov 2025 07:26:57 GMT  
		Size: 1.9 MB (1926843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f8d4793d6aef147950d659fad56f48b41f8f8db25f38a3650abd20ecd28d7e`  
		Last Modified: Tue, 18 Nov 2025 07:26:57 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6cd8d0669f5f5748f133a5e6947d883cfe5821d2e7d6d4f6140da554b7be8f`  
		Last Modified: Tue, 18 Nov 2025 07:26:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8955a5a1e6fea2e282e120fe40533c301d077afb15055b98c12cc1513f239`  
		Last Modified: Tue, 18 Nov 2025 07:26:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aa8ba8dcf7866c5ebcb2b09562fbcdc1766edeb354f9f0a5a2284a253419ab`  
		Last Modified: Tue, 18 Nov 2025 07:26:57 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:20ecb37eaf19143cd2286d92a52af8e8a84c81d946e9b790c4355bae05e54597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d309cc8083b5734b5ee778ac5258f8286989b55c33074ff86be1fbf969a090a`

```dockerfile
```

-	Layers:
	-	`sha256:9aa87e7927d0f73c936b00e07962ce93a4cd38e8e3cb89701cd99789286badcf`  
		Last Modified: Tue, 18 Nov 2025 10:54:29 GMT  
		Size: 2.1 MB (2100948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28e482ce455eae1f93ef7281cd8546a710ab4bb19435b7dc705a020572a97d0`  
		Last Modified: Tue, 18 Nov 2025 10:54:30 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json
