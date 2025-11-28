<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.7`](#elasticsearch8197)
-	[`elasticsearch:9.1.7`](#elasticsearch917)
-	[`elasticsearch:9.2.1`](#elasticsearch921)

## `elasticsearch:8.18.8`

```console
$ docker pull elasticsearch@sha256:e5b3511e96ee1c58e9027d9d06185be4e627074717b40f6145e860b39c851d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:35ecc9ceafc87e7e60973f820793db03c21af60410daea2b4b8b6f192e06a5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.4 MB (699422102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc452320d24ce506503a786fbb099915ccfda188e38dc39ee9a02e904db4356`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Thu, 13 Nov 2025 23:22:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:25 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:25 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:25 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:23:55 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:23:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:23:55 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:23:55 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:23:55 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:23:56 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:23:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:56 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:23:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c43ef599f7a98ef31360bd3771828770c70193f3b08e03430ff63352d1879c8`  
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 4.5 MB (4493909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f7b345db94a1a2c86c7e241bac630afd7c708a4540a5db8ca5523ac1da61e`  
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 3.5 KB (3534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27b11736af81fe4f0c3b5bee6534722ce2b0f084588d47dad6966c0aa4a6a1`  
		Last Modified: Fri, 14 Nov 2025 01:40:46 GMT  
		Size: 664.9 MB (664908814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b46a367471c93768bfac25f1547059ab2f1bd1d200cd2dd370fa11b9b2cc37`  
		Last Modified: Thu, 13 Nov 2025 23:25:04 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c0aa5ff83b648b37592a0d6e8d0e888650d97e71e606cd607eb29692d0518`  
		Last Modified: Thu, 13 Nov 2025 23:25:04 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41db951a09358077109950cd0cfb24fbec2a7dc5690e9175a388b6d00fcd5089`  
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 163.9 KB (163935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff2aa099f19d62676a29e3ec7f8b2874349672def2cf3b834fffea50c6e4ae`  
		Last Modified: Thu, 13 Nov 2025 23:25:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b1972ad4e20e050b4102887185fea470d4215100c4aba3d82cb6fb1e637812`  
		Last Modified: Thu, 13 Nov 2025 23:25:04 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d0daf70580c4cba91cdd0ed4c6cd71677db0c923a8027ba4b75aada7a6a2f4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae5830d902bc2d758204867320ea83541a43eb19bb1fa7696bccf0881186a96`

```dockerfile
```

-	Layers:
	-	`sha256:9995af78231b89816a76739c50ba1f806a2cc015d6ae90cf0842586906d04931`  
		Last Modified: Fri, 14 Nov 2025 01:25:30 GMT  
		Size: 3.2 MB (3192944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436e294639573790ef3eb79fa2513fd3c74f12f8bc626acfdb13396b89cfdca8`  
		Last Modified: Fri, 14 Nov 2025 01:25:31 GMT  
		Size: 38.3 KB (38346 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:488365ccd5c96cc323443fb11f05caa6f38a92478f0ed0d20720e8ceef06b533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.7 MB (541654815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e5c1d0847c150e67ed3e57c8b83555a6f7f8a8cc7c205333eefa45f3a239f3`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Thu, 13 Nov 2025 23:22:07 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:07 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:07 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:07 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:23:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:23:12 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:23:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:23:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:23:13 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:23:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:13 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:23:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc64f53563943fb470824b87140561802dd52d43f4628eb68bb7fa8f57a0b5db`  
		Last Modified: Thu, 13 Nov 2025 23:24:07 GMT  
		Size: 4.5 MB (4498895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f44bc7b0af09b3a694a152f1433649cc2cbeb6f770e442b41bec589997f56`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9728459a5a3f4abb547584c07ae44961768661babd029b4713cb12ae80e9924`  
		Last Modified: Fri, 14 Nov 2025 02:55:02 GMT  
		Size: 508.0 MB (508003274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d526010e9271cf1fa50c3ce58b45edc2baeb72f63c9103694e37f4077e63a15`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f26d3872bef9a883c14b822ea082a9dbe814100cdcb33e6651be5133102f3a6`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e542b2865e2c21d02b52969930d99a03a04fe759cdd4f2d2ce726640d3d37bdb`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 160.4 KB (160368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c191344f90bbd2a51a6f8d0bab30596843eca8331bfbc68310678792d9bba0b9`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057047f0e243f23a7af94bfd9a04e48c031c234ab097c42fb5345c01e0f4f118`  
		Last Modified: Thu, 13 Nov 2025 23:24:06 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2c61bcff8d19e16d5e371f6d67e44c05122a20062a9bc9497c13d439273794c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c2c1559c8e3e5b599c799acab4da7a6849233e298853011329c3bf143ef2d8`

```dockerfile
```

-	Layers:
	-	`sha256:7be2357a91cb793fac5a7b45556077661c810924e084b5530d9a0af487cc5806`  
		Last Modified: Fri, 14 Nov 2025 01:25:36 GMT  
		Size: 3.2 MB (3193357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b82cbadcba6dca71ecc5d86882b31ebb377b61b1f4ba16d2605bc675a987df`  
		Last Modified: Fri, 14 Nov 2025 01:25:36 GMT  
		Size: 38.5 KB (38548 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.7`

```console
$ docker pull elasticsearch@sha256:ff698b2f7dd37c8b7517a73194559d604e6568b3882af05d8190a2d5244c1988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:32a9715a88879b61b93da5f057a1b6d097dbdacf1232ec0cf84358e3616dbedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.8 MB (706830529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cd795a3b5d5dea733f4239c0338f16d6182c7fd4c31d4cd73af5eb24e354ec`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Thu, 13 Nov 2025 23:22:31 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:31 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:31 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:31 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:24:03 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:24:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:24:03 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:24:03 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:24:03 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:24:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:24:04 GMT
LABEL org.label-schema.build-date=2025-11-07T13:35:54.762042224Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=198d86868932741b4e0d184425510217febc27d1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:35:54.762042224Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=198d86868932741b4e0d184425510217febc27d1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:24:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:24:04 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:24:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eedf2cb97239fee53fa50bcc02e66327659cb1e53544a9294513f1ed881ec6e`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 4.5 MB (4493928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7510353cd2679ad87546d0043d91cab8a626eeb49ef21c6b8087d4e34e542e`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b579f6be3438fae726b022e5cdc4345daf7925027e9476d295117f7b853f0201`  
		Last Modified: Fri, 14 Nov 2025 01:30:03 GMT  
		Size: 672.3 MB (672317228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed55c1ff45199138809922057270d3b955e8235b81ffdaa11d8e3898a03e857c`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec5d0f363c674cd5224287f26102f06e681532e4cde073e8ab837b64cca6c3`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e41eb3f0160f8d319d6bb033453df01b901fa678a2512735b5e4078c16c99f`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 163.9 KB (163936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93004e76c5cc12a458e548c1dabbaf000e8546096f876ed2657525cacf32eb9c`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4b73630156627ea04b267c9f185cf70d5f4feb7f30bde2b765988cbae974e`  
		Last Modified: Thu, 13 Nov 2025 23:25:19 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:510811dd5bbab1a99a4641d620afaa57dc2c10b1663e387236c07310370be3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d20df509ae3e7e3cc970113ae1808075d7872e0568c89e62011404c894f7a1`

```dockerfile
```

-	Layers:
	-	`sha256:4dbe87d60eadcd0ac2e6fa4554cf784c73c9b8fdadea03efd1fe1cca3791cf09`  
		Last Modified: Fri, 14 Nov 2025 01:25:40 GMT  
		Size: 3.2 MB (3215994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209650b0846ff2dcf6605a414d4391dcd69497bcf300a37c9a8115a450a08a95`  
		Last Modified: Fri, 14 Nov 2025 01:25:41 GMT  
		Size: 36.8 KB (36840 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e9849d694a27ed0427df5a2b83621057f8129d974f93b4b05b6c9578491c3f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.0 MB (549047435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2226b55500b37fcfe688d6cfeb27c4a57240108c74b983319ecb1581d4477aa`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Thu, 13 Nov 2025 23:22:15 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 13 Nov 2025 23:22:15 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:22:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:22:15 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 13 Nov 2025 23:23:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 13 Nov 2025 23:23:20 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:23:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:23:20 GMT
ENV SHELL=/bin/bash
# Thu, 13 Nov 2025 23:23:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 13 Nov 2025 23:23:21 GMT
LABEL org.label-schema.build-date=2025-11-07T13:35:54.762042224Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=198d86868932741b4e0d184425510217febc27d1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:35:54.762042224Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=198d86868932741b4e0d184425510217febc27d1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:23:21 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:21 GMT
CMD ["eswrapper"]
# Thu, 13 Nov 2025 23:23:21 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5dc2b0d5e559cfcb00c026e4821bafbf21b712d0bf5b2dae416e038be43066`  
		Last Modified: Thu, 13 Nov 2025 23:24:17 GMT  
		Size: 4.5 MB (4498781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a529ad298c4b710fb7ec862b44a7a661935eb5a73655ffce521073802ed3ba`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6c03c065daeb81cc8b7c15141229a93cd14aa49c7b091fbc57c6458c45dd6`  
		Last Modified: Fri, 14 Nov 2025 02:16:08 GMT  
		Size: 515.4 MB (515396014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369fca0716a1d41a91e8317b6816825ad75030e323ac3470d0244d34cc95c998`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3b7cf8e0dd9b3b69416d9dd1dd2551bd0299f61a769ba6849354d09b8e9a9c`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8955afe7bb1d0b05dcd79e2f203d8136c27c2863c8a4cce7fcd5a9051d4a4f74`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 160.4 KB (160365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1117e6b09102410992e67ecf06fc0104bdc33d3e7787278a1c0124271dc28`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049b864e3d605dd66c0a078becc7cda1505f4eda3c71e22c6cf5af999a9cf9b0`  
		Last Modified: Thu, 13 Nov 2025 23:24:14 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:23d662ec26f67ac7c4912df55daf57bdd9aaf306b82c105e914a6f36c9265140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ce87df191f61141850731d8170a4c14ed1daa7f9992dd6be2d1341b53a0567`

```dockerfile
```

-	Layers:
	-	`sha256:9cc1ff05f03678690f4144529afd86bc02cb841ca1eb370163ddadebe57b5c39`  
		Last Modified: Fri, 14 Nov 2025 01:25:46 GMT  
		Size: 3.2 MB (3216407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5059f722d6b952bb3a2b01fefb3882703fb3b7930bc9715928e946483618b9f3`  
		Last Modified: Fri, 14 Nov 2025 01:25:46 GMT  
		Size: 37.0 KB (37043 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.7`

```console
$ docker pull elasticsearch@sha256:ed4a3bb79bbb7198d206156b22bdc57707f1f41cd0c7e946d02f74b3bd80ce15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:64592cfb6865e7a91dad6d9bd3831f72953585979b53d969e60f156c2fbe61cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.3 MB (727335388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc13cea5852f15b0767f6b1b6ec5e389506940fb6e021be24fe8efe14fa6ef2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Mon, 17 Nov 2025 23:17:41 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:17:41 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 17 Nov 2025 23:18:57 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:18:57 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:18:57 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 17 Nov 2025 23:19:07 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 17 Nov 2025 23:19:07 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 17 Nov 2025 23:19:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:19:07 GMT
ENV SHELL=/bin/bash
# Mon, 17 Nov 2025 23:19:07 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:19:07 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 17 Nov 2025 23:19:07 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 17 Nov 2025 23:19:07 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Mon, 17 Nov 2025 23:19:07 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 17 Nov 2025 23:19:07 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:19:07 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:19:07 GMT
CMD ["eswrapper"]
# Mon, 17 Nov 2025 23:19:07 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99c39ac1269673e4d333cb91d222ef220b7b76dfbf90f171aee242e3d19ee7c`  
		Last Modified: Mon, 17 Nov 2025 23:20:20 GMT  
		Size: 4.3 MB (4288243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f5a2865122f362a57d5b2d47ad602edaf645b1e28ce472109f69925f9b1409`  
		Last Modified: Mon, 17 Nov 2025 23:20:20 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503e7dcaebd9c282eaecf9cfac40a79c8d8937b282940b4820f39cd5395f7111`  
		Last Modified: Mon, 17 Nov 2025 23:20:20 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d186954ca58bb0d885fd3f6f69bdd68fef4552b3aa0a6b28539698f650f61e6d`  
		Last Modified: Tue, 18 Nov 2025 01:40:45 GMT  
		Size: 683.0 MB (682977725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71acec528d0ee06cd13ffe917e688824e365fe1634889f3cf80f1c461c83f115`  
		Last Modified: Mon, 17 Nov 2025 23:20:20 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c4b53fcbe7a2f15159ea1e68a1a4d82acf7d35b719510cba81bb7b6b3d40e8`  
		Last Modified: Mon, 17 Nov 2025 23:20:21 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0714b2a181ecbbf5242f73e2d12aecd410dc6c72d1324ec67ddee570dc4b3e`  
		Last Modified: Mon, 17 Nov 2025 23:20:21 GMT  
		Size: 75.2 KB (75183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fac6e77bf489e07d45d5537937795e3d7ae506ff9832e86a6747e4f13293d7`  
		Last Modified: Mon, 17 Nov 2025 23:20:21 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6ee97b3e265b3f6eda0e4a535a78912197e4d2d51176b8caa8e041c4c2d3cf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5e4c76a122a8c7c8615d5d41cb7ea5887ce2deb2a9e4f68d8dedc62f40f79c`

```dockerfile
```

-	Layers:
	-	`sha256:9bd0e83c65aeee46652209b6c66f4b3f453af1c66b7e6631b1c029f90dc25294`  
		Last Modified: Tue, 18 Nov 2025 01:25:22 GMT  
		Size: 2.1 MB (2091577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a08b9bb0e64027f0adaa6921a67cf755191066ddebd6fcf388a8aa4b31b365f`  
		Last Modified: Tue, 18 Nov 2025 01:25:22 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:bdc3422dfd80b00731c1cff282a71a841605049dc9f5018a5a7e31b44c1eff83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.6 MB (565636482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf283c4f9fa70bfe5568e5d0ba3b228a65b35fb9430c0f692eac1610bc3166`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Mon, 17 Nov 2025 23:18:13 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:18:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 17 Nov 2025 23:19:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:19:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:19:09 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 17 Nov 2025 23:19:15 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 17 Nov 2025 23:19:15 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 17 Nov 2025 23:19:15 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:19:15 GMT
ENV SHELL=/bin/bash
# Mon, 17 Nov 2025 23:19:15 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:19:15 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 17 Nov 2025 23:19:15 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 17 Nov 2025 23:19:15 GMT
LABEL org.label-schema.build-date=2025-11-07T10:07:43.588125290Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=49e091e266fdfecd2b3a96f9d390719838fb742d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-07T10:07:43.588125290Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=49e091e266fdfecd2b3a96f9d390719838fb742d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Mon, 17 Nov 2025 23:19:15 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 17 Nov 2025 23:19:15 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:19:15 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:19:15 GMT
CMD ["eswrapper"]
# Mon, 17 Nov 2025 23:19:15 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513692dec6d5cbe39c614125b131f1cfaabe313ca39d79a4b1af08dd35dc9e47`  
		Last Modified: Mon, 17 Nov 2025 23:20:11 GMT  
		Size: 4.3 MB (4301047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f839f758f72690ff6cbdcfc7eafa782f679ced62601ba12de6e3e8c66c250f04`  
		Last Modified: Mon, 17 Nov 2025 23:20:10 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220e8c0f0ecb35d3f580e0923c0f915db780360a41849e23726767f7a3ae844`  
		Last Modified: Mon, 17 Nov 2025 23:20:10 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27893b26bb5948fedaab374b8191c69bedcee2b43bcad52c8d67ae3e471b94f`  
		Last Modified: Tue, 18 Nov 2025 08:07:32 GMT  
		Size: 523.0 MB (523046688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee79190daa033e3e4ffcb75934d2483db10c65202b522928277e6192bbf1f41`  
		Last Modified: Mon, 17 Nov 2025 23:20:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f09b2e5243c578bfc3e6a6ee209b5d753e30678fed22a2103d3d0bf3581593`  
		Last Modified: Mon, 17 Nov 2025 23:20:10 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa2dd29147c834dda287838dd7cff8d0a61a4d72b2961283f6a91f804bad7a`  
		Last Modified: Mon, 17 Nov 2025 23:20:10 GMT  
		Size: 74.1 KB (74110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb227d24ceeeade26885e9cbd9d959e8d7d284fb6a91dd2d6fe758970eaf4973`  
		Last Modified: Mon, 17 Nov 2025 23:20:10 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9f789a2591c69f4f69b9f96ebfe95e7092f038c2ecbd87a0390e784280814774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01d368df566f062dab847fe3d78e674104cb35d0c4e8d664fe86c35438543e4`

```dockerfile
```

-	Layers:
	-	`sha256:3ae74dcfcd65f6f0e390847f6109eef932d8a3be3e71b29bd5d673bff7aceae6`  
		Last Modified: Tue, 18 Nov 2025 01:25:26 GMT  
		Size: 2.1 MB (2092139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68f9e74306976327d3df5b07a687425cc5af86666a310165045e59326810112`  
		Last Modified: Tue, 18 Nov 2025 01:25:27 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.1`

```console
$ docker pull elasticsearch@sha256:872127ae799a4bb8a9c1a9b112d1670a27e2c31815a3965bb455c2b21e31b0f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:1beab9fed9312598b1b661cd05c5b54e9fae84b5b67f7611ac27dc96c9694455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.1 MB (737102045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7aa1c2ec32181590f7cf8b2c19bcc2eca418e6f685113040d51c9278d2af263`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Mon, 17 Nov 2025 23:15:17 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:15:17 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 17 Nov 2025 23:16:33 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:16:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:16:33 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 17 Nov 2025 23:16:43 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 17 Nov 2025 23:16:43 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 17 Nov 2025 23:16:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:16:43 GMT
ENV SHELL=/bin/bash
# Mon, 17 Nov 2025 23:16:43 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:16:43 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 17 Nov 2025 23:16:43 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 17 Nov 2025 23:16:43 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Mon, 17 Nov 2025 23:16:43 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 17 Nov 2025 23:16:44 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:16:44 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:16:44 GMT
CMD ["eswrapper"]
# Mon, 17 Nov 2025 23:16:44 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e557ec91e8aff3c377b564d8b3c8d810194b4d3688f1218e41456418b405e027`  
		Last Modified: Mon, 17 Nov 2025 23:17:57 GMT  
		Size: 4.3 MB (4288259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c24a52584756c9480c8088103abe7da7b92ab66d8357e9a3c9a8a57c63316f`  
		Last Modified: Mon, 17 Nov 2025 23:17:56 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887a27c7bda1b952262d2e13fbc58811c1ff3f3a0aa79659d3c5bb36b3226ab0`  
		Last Modified: Mon, 17 Nov 2025 23:17:56 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa3077a4065b9e9d13bdf7cadca7434f670ad393ca5fda1aeb4f1fb4ca62fee`  
		Last Modified: Tue, 18 Nov 2025 01:28:45 GMT  
		Size: 692.7 MB (692744366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8c1a0b3c3aa9dc6ed448085d72753b654118eaf2a83ff4f0133cdcb899d980`  
		Last Modified: Mon, 17 Nov 2025 23:17:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6607e66cc46f87308c861d9c1ee6cceef05b47bed3927485825cd86c0b9daa`  
		Last Modified: Mon, 17 Nov 2025 23:17:56 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9192563cab5da2fe2805b3d556e962acaa94bd45e45d2dca829da7888bf5fa`  
		Last Modified: Mon, 17 Nov 2025 23:17:56 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296dca031d482f46fb99be5cea32e0e6de648f551d664524d8809947e473b040`  
		Last Modified: Mon, 17 Nov 2025 23:17:56 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3fe5b7ec12127e40ada2e12c0d6ec4691587c46e0a7654d2e0a2e6c13dc2a6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60742488e6dff58dfa9c73850932c49e808041878b567ece476a90445379120`

```dockerfile
```

-	Layers:
	-	`sha256:358053f4f7fc11517b23f76e4a5f6bd75c9f64d71d4c5106cf33b4b2296e25da`  
		Last Modified: Tue, 18 Nov 2025 01:25:29 GMT  
		Size: 2.1 MB (2097824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ceefabc3a9fd4698324d8b4dcdbe804215cd0b2f81a48b59eb49432f6ea2a7`  
		Last Modified: Tue, 18 Nov 2025 01:25:30 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6b49ffcf9877e2d0cb9839461156ac903c982dd95dd97e0924ca959d28eb6f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.1 MB (581127082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f9586a488522ddc771d72e4c931f9856edc1dd6187b2ca58937635b1e079fc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Mon, 17 Nov 2025 23:18:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:18:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 17 Nov 2025 23:19:18 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:19:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:19:18 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 17 Nov 2025 23:19:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 17 Nov 2025 23:19:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 17 Nov 2025 23:19:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:19:24 GMT
ENV SHELL=/bin/bash
# Mon, 17 Nov 2025 23:19:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:19:24 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 17 Nov 2025 23:19:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 17 Nov 2025 23:19:24 GMT
LABEL org.label-schema.build-date=2025-11-06T22:07:39.673130621Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T22:07:39.673130621Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ad0ef0e98a2e72fafbd79a19fa5cae2f026117d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Mon, 17 Nov 2025 23:19:24 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 17 Nov 2025 23:19:24 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:19:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:19:24 GMT
CMD ["eswrapper"]
# Mon, 17 Nov 2025 23:19:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5633e99a6b45453b38c6dc2af28ce5a4258f8985aa3377efc498e98932bd267c`  
		Last Modified: Mon, 17 Nov 2025 23:20:31 GMT  
		Size: 4.3 MB (4301089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fcfc93b5a4066d70c6e8289521275eb1da79b04e0893be11a4f1af831682f9`  
		Last Modified: Mon, 17 Nov 2025 23:20:29 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad582adfddbec80e8560458a2c23d367ec036e3968edee6723895c1a3b57e53`  
		Last Modified: Mon, 17 Nov 2025 23:20:29 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a019f6a0924dbd54e19dbd1a1366338ac9426b8467ddd926c9129be90787e8`  
		Last Modified: Tue, 18 Nov 2025 01:44:11 GMT  
		Size: 538.5 MB (538537244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b15f0b80a74c9d9299758ba8487dbcbd705cab84cb347a5df32d203d1925dcc`  
		Last Modified: Mon, 17 Nov 2025 23:20:30 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb12b08c71f279a4a534b87831c3bae4de534a32bcc59cfb2adcf5b19cb826e`  
		Last Modified: Mon, 17 Nov 2025 23:20:30 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a61db182e2c05ec808eaf544fec75436dfd1f70fc1c653f5da7891f5436c2a`  
		Last Modified: Mon, 17 Nov 2025 23:20:30 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229c5bcdf4a78b62301e08cabb33ed6ab281a764d0b3011f4ff3b0989a6b7c0d`  
		Last Modified: Mon, 17 Nov 2025 23:20:30 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:817ee7bdff4f67925aa7b535678474b3dfbad265014b7c72d4a19e0932191b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c9b5364ab00e85afa870c8e2a156f3bb41d7f9ba541321140267106c429c92`

```dockerfile
```

-	Layers:
	-	`sha256:9bac7dd155bc4772d95ed8286061562e1b217eb4e610bc627df4192df0e2ef22`  
		Last Modified: Tue, 18 Nov 2025 01:25:35 GMT  
		Size: 2.1 MB (2098386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e039e7e4f3354d4fea5bf0b0b4a3195a1f72fb9dd1776ef60cef7e1867ced7b3`  
		Last Modified: Tue, 18 Nov 2025 01:25:36 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
