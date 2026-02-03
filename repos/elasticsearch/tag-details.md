<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.10`](#elasticsearch81910)
-	[`elasticsearch:9.1.10`](#elasticsearch9110)
-	[`elasticsearch:9.2.4`](#elasticsearch924)

## `elasticsearch:8.19.10`

```console
$ docker pull elasticsearch@sha256:c874f965dd6fac82e185f871bbeaa1a51d65e2e6b97d71fe3201dfdd242fa77f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9e5d1d7fa7928bcbc1c16a6a51064d83aa13b0ee2e269366fb44408c118afddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.0 MB (710000547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0227f6f66638aad46c53e85299e287b091b2d9ef78ff9a2da837fdf9c4c0ff28`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:52 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 15 Jan 2026 22:20:52 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:20:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:20:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 15 Jan 2026 22:22:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:22:26 GMT
ENV SHELL=/bin/bash
# Thu, 15 Jan 2026 22:22:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:22:27 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:22:27 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 15 Jan 2026 22:22:27 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:49.939644068Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=493241b351be6d9f40d52a1406c91a23b4148821 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T22:07:49.939644068Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=493241b351be6d9f40d52a1406c91a23b4148821 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:22:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:22:27 GMT
CMD ["eswrapper"]
# Thu, 15 Jan 2026 22:22:27 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c03eb992d21b08630d8ac503049a8718241ad97aa496f65e86ef83ecc4c9fda`  
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
		Size: 4.5 MB (4493983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80192c435f327724f0c26bc4cb00017e19aa75844ed49a17bbabbf1b5a144ada`  
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129766b9837a8a879dccafbe827bc492df6ba46b5db573a26bc6dbc9a819ce9`  
		Last Modified: Thu, 15 Jan 2026 22:23:31 GMT  
		Size: 675.5 MB (675485875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f857c18cb177c30c3e7cc8702c6d04273239f4c80660f2ea9eca9a1b55a6376`  
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08e04d847400c4c6f3bc7d61f5580811f6a37a8e5ad5b79179b73883072447`  
		Last Modified: Thu, 15 Jan 2026 22:23:20 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72d8b944558d4ac06b4eac8fb20864bcc70746e2c9132d8fb6079f0afc3498`  
		Last Modified: Thu, 15 Jan 2026 22:23:20 GMT  
		Size: 163.9 KB (163938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acdd356e40bdedc39ff6be28c27c0f23c3603600e03721f26f3cb50e1d7d2bb`  
		Last Modified: Thu, 15 Jan 2026 22:23:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c906ecd5f0ac59a48c57178aa8bda7a96462366fa3e6add01bf6f32bdc41fd3`  
		Last Modified: Thu, 15 Jan 2026 22:23:21 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ab2210830ccfe04411aea858c47ae8ae0b3dacb9e1f0ad9449120d390d5805e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac7d496b691da1d07c5dd85de3d34cc7f7dceb9140fc5bcb7adc7f07020969c`

```dockerfile
```

-	Layers:
	-	`sha256:a8b98cb8971682b716b25524ec20fea3f4ee4a4b930dfc324a22a10b4649b519`  
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
		Size: 3.2 MB (3210136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d72ff81f2cafdf8acc84318265f241bcf9ce95f7eb02a9b2b268bf4f5baf670`  
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
		Size: 36.8 KB (36847 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:dce6afcf35b7496c9256f3b96bb70c45884bbbe265ee00679e21698a3ec274fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557805676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e39a33aefe5fb61bcacd1bdbf795f95890678c53414afb221679b6910731fa5`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:22:28 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 15 Jan 2026 22:22:29 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:22:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:22:29 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 15 Jan 2026 22:23:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:23:34 GMT
ENV SHELL=/bin/bash
# Thu, 15 Jan 2026 22:23:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 15 Jan 2026 22:23:34 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:49.939644068Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=493241b351be6d9f40d52a1406c91a23b4148821 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T22:07:49.939644068Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=493241b351be6d9f40d52a1406c91a23b4148821 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:23:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:23:34 GMT
CMD ["eswrapper"]
# Thu, 15 Jan 2026 22:23:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cecb70ace38b5cdee15860059283a295171284116b721c39afdd3955e94530`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 4.5 MB (4498888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e4f5581ba049194157cd8d6ab4e92232b4aadb1ae418aafe5ba0de22bfe8b`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 3.5 KB (3524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e8ebd0db0bab4c12e2ef0315c656b022253aba7d11a10db6bcff83aab6658a`  
		Last Modified: Thu, 15 Jan 2026 22:24:21 GMT  
		Size: 524.2 MB (524152275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139356fa507a6e45e98749dcefde6b35c512077019929d5f71d22de5b562bcfb`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff06542254a202e810d0bb4e785ba6109267574b5b49db0471f1e0990d51af`  
		Last Modified: Thu, 15 Jan 2026 22:24:13 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e6a44bee32fbf11cd824cfb3c864c868121d59824f2cf524186a410d7a2e3e`  
		Last Modified: Thu, 15 Jan 2026 22:24:13 GMT  
		Size: 160.4 KB (160371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8303504bec948635617643b12f7cddc08d918a5db8e0e02352ace66e58b26062`  
		Last Modified: Thu, 15 Jan 2026 22:24:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f173cb2734f3479d8b874acef3ad9bee91b002aea67b734ef29c5d8b3295037`  
		Last Modified: Thu, 15 Jan 2026 22:24:15 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4a6b755816aced0923a319b912ed26259d366b246d69a16850424c1aaa8713fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3247599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e086ba01be4ec42db4ce99886c1232e2d33e3e84750443b7440a4a6b3b6013fe`

```dockerfile
```

-	Layers:
	-	`sha256:c98a7e76e13f71ef00ae7629b1061502a5b1865e1915ab46cb78065798e26714`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 3.2 MB (3210549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ac5a82768f0b4690c0738d180d0bf35de57e76fe7b0c62aa0fdd64c37857f1`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 37.0 KB (37050 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.10`

```console
$ docker pull elasticsearch@sha256:c1fd1b6a09000283ecdf036113c77bcff64c40c34772d23d04a0a125527ce5ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5a603b560c539b8930a78cb1a93446ec005661dc3ee881e17cd65c73f9a9118c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.6 MB (730643051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623e8207579cba6d8b40ec93d03c5220e0b12f0e40400f6f5b8d27398206d39`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Mon, 26 Jan 2026 22:05:29 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:05:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jan 2026 22:06:54 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:06:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:06:54 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jan 2026 22:07:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:04 GMT
ENV SHELL=/bin/bash
# Mon, 26 Jan 2026 22:07:04 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jan 2026 22:07:04 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:07:04 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 26 Jan 2026 22:07:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:07:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:07:04 GMT
CMD ["eswrapper"]
# Mon, 26 Jan 2026 22:07:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21efb3ee2d6e5b6a6f847b91b53d0720e20ec04a32edf5e3f2afe6cd6c3962f2`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 4.3 MB (4286292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309687df99ca8a16d2eb6713e5e524d6be56a817e9d4e62a0eb6e198fbcf8d5`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc8395d188d85a869d09c3b38732e3076ea72628ab627aabdecfcffd8c7cf2b`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9abaed0152751cd0fd394a766ea16c2acbd495dbc670724183763fb1b4b989`  
		Last Modified: Mon, 26 Jan 2026 22:08:09 GMT  
		Size: 686.3 MB (686261779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dbbf014bebb14d21319b980356fecd96c1557d8d9a5b9dcea79e8db5c3b735`  
		Last Modified: Mon, 26 Jan 2026 22:07:58 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558f50c4fd45cd06bbb4836375a832f317ef0bcfa9d721a1b1a7982c3d54dfd`  
		Last Modified: Mon, 26 Jan 2026 22:07:58 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b487f353f99170ce8e2d0d23edefb6990361f1e5c2530ab982f45e1b8709cd`  
		Last Modified: Mon, 26 Jan 2026 22:07:58 GMT  
		Size: 75.2 KB (75180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e76aa407a5de5aacad7cdf902d36e4a42e83af6679fd7631c6aedf87e12190`  
		Last Modified: Mon, 26 Jan 2026 22:07:59 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6515cd966003bbf78302450b2ec1b2c35e832e076cee1ccf6f6a3e23ad6d591c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75343c5d77ab3a87b7e58a1e74213f163a6ca7bf88bdf1d4c6d3154af142f180`

```dockerfile
```

-	Layers:
	-	`sha256:f628c1425b8d92cad255acfe9ce6a184ccf0eefd0b562ee3a55bb6766ca07ae4`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 2.1 MB (2085728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42da45dd5023e71fb7f29ff10b1569acf74da7669c826a7d01700c7cf4cd9f93`  
		Last Modified: Mon, 26 Jan 2026 22:07:57 GMT  
		Size: 33.9 KB (33867 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:362331d217721a8301fe41239a3ed2349ca90eaad69879a52fa63d7f69edd442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574629943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e543e94a502d9faffd908acd4fa4f1afb206f35e06cec0ce3ec41059e027185d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Mon, 26 Jan 2026 22:05:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:05:27 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jan 2026 22:06:22 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:06:22 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:06:22 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jan 2026 22:06:28 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:06:28 GMT
ENV SHELL=/bin/bash
# Mon, 26 Jan 2026 22:06:28 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jan 2026 22:06:28 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jan 2026 22:06:28 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:06:28 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 26 Jan 2026 22:06:29 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:06:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:06:29 GMT
CMD ["eswrapper"]
# Mon, 26 Jan 2026 22:06:29 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fede9481ad2d2a5daa610d3a860308b3b04fd5caf79669738d934facb1e1ea80`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 4.3 MB (4297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ff6a49150a7a19feb4325a929fbc437bcc07f08104303a65dda49145ed59b`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc57f21a3870c175c73e605cab60c338a56b7bbe63d7f0d4cca6816e8909cce`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463893edc47350d18a0d6ae2732d0625a2e63cbe39282440ac1740e21f2ac9e`  
		Last Modified: Mon, 26 Jan 2026 22:07:17 GMT  
		Size: 532.0 MB (532020336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d4643b1cd331424d5a050620eb07118fd4b22931af8dab28de9f7c6b9e9f49`  
		Last Modified: Mon, 26 Jan 2026 22:07:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d812254818aa2f494ce706b8d618298f3f674335b5213866463cb5d2b65e582f`  
		Last Modified: Mon, 26 Jan 2026 22:07:08 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a284f6ab5c54d7cd3035bc42a0d0757ddc751bfe2e57fac6d1db3816504f391a`  
		Last Modified: Mon, 26 Jan 2026 22:07:08 GMT  
		Size: 74.1 KB (74105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c1527291a7227ad3c0e38fd380c47f57394d970d7598e7b9f50a84efec6dcc`  
		Last Modified: Mon, 26 Jan 2026 22:07:09 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:091165220e12fa6c314f59dd306c7be4bda6bc3826c0dfe349a9bc8f1f45ca2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d706a097e4c547633df13622e6fe20a111f0a71d8d0651420a50d2288a690a45`

```dockerfile
```

-	Layers:
	-	`sha256:a0643e052a5145169bb6078d245514febd8593d0eba5dbb4b7f3749306a1e68a`  
		Last Modified: Mon, 26 Jan 2026 22:07:07 GMT  
		Size: 2.1 MB (2086290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6601eb7421be145a20cb4b4fa58cab6e154884483f4a5f70188b8c22b0125785`  
		Last Modified: Mon, 26 Jan 2026 22:07:06 GMT  
		Size: 34.0 KB (34049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.4`

```console
$ docker pull elasticsearch@sha256:ba3ca06dc9121baad53ec025c87eef9352fcae11d89cd2e4cba8821977e81319
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:38d7791a8f9bbe53f907cff922aac15061e0f2ec4485dcd1e47c423f5f0aef20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738179205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281772040f2667151746d7dbba5b6785d5853b1755932dc1f9e1c947fdfb4352`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Mon, 26 Jan 2026 22:05:34 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:05:34 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jan 2026 22:06:47 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:06:47 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:06:47 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jan 2026 22:06:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 26 Jan 2026 22:06:56 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 26 Jan 2026 22:06:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:06:56 GMT
ENV SHELL=/bin/bash
# Mon, 26 Jan 2026 22:06:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:06:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jan 2026 22:06:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jan 2026 22:06:57 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Mon, 26 Jan 2026 22:06:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 26 Jan 2026 22:06:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:06:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:06:57 GMT
CMD ["eswrapper"]
# Mon, 26 Jan 2026 22:06:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5ab85b82f825bdcac558ae916404098cc8a558093f31517603e584d1dc8986`  
		Last Modified: Mon, 26 Jan 2026 22:07:50 GMT  
		Size: 4.3 MB (4286266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f37bcb783f4bb54daf2436279ca9c61d0cfb64e1fae771fa74b641e626a9ee1`  
		Last Modified: Mon, 26 Jan 2026 22:07:50 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47e8ef18f1e452cb4113c397bc46ab0314319fc70ca582d43554d2e8d7f86d7`  
		Last Modified: Mon, 26 Jan 2026 22:07:49 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b8f03e94e272ee97fea1162c9e5181f4d2311d83990f1d12172bf4b08be6ca`  
		Last Modified: Mon, 26 Jan 2026 22:08:03 GMT  
		Size: 693.8 MB (693797960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fd1af1347edfaf5320c4056fc81af4098a9378f8f1c42719b0eb692aa99172`  
		Last Modified: Mon, 26 Jan 2026 22:07:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cb836c22f03f9d14fcb89964bd3e8f65e0dfee2cd110df7211e00d578128f1`  
		Last Modified: Mon, 26 Jan 2026 22:07:51 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4cf46958f05dd7d593f0f54e56deffb7b09303f8dfd58fa2e552303db6056`  
		Last Modified: Mon, 26 Jan 2026 22:07:51 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa582dc6ed1f3bdb359d941e1227e783fa8b07b6479660fd1ae8e4d55a5aea15`  
		Last Modified: Mon, 26 Jan 2026 22:07:52 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5fa790a0732fc94f3cfcd2a36938e404b09d571e37c26e21e127c7fa0a4504ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fadc2b130df11e168e1ab17e446369e32e7a7afd29226ccf98f5aeceef87552`

```dockerfile
```

-	Layers:
	-	`sha256:a55535e8428fdb87141e4908770a0543678cf7df660d20c91464e3bf3eed30a4`  
		Last Modified: Mon, 26 Jan 2026 22:07:50 GMT  
		Size: 2.1 MB (2098087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4cc9cfb92e82fc35125219f0ccb07d14407a05a8d42637152c92560459be4d`  
		Last Modified: Mon, 26 Jan 2026 22:07:50 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ae29c0f24b8125548c44f102aab8b7a665c351f4ca975b969a0e613261aa02f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582193280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc79ff2c69d606cb7ad63189ac6d78ab7d19bba87cad750c3fb1c4b29188a98`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Mon, 26 Jan 2026 22:05:32 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:05:32 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 26 Jan 2026 22:06:26 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:06:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:06:26 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 26 Jan 2026 22:06:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 26 Jan 2026 22:06:33 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 26 Jan 2026 22:06:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:06:33 GMT
ENV SHELL=/bin/bash
# Mon, 26 Jan 2026 22:06:33 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:06:33 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 26 Jan 2026 22:06:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 26 Jan 2026 22:06:33 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Mon, 26 Jan 2026 22:06:33 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 26 Jan 2026 22:06:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:06:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:06:33 GMT
CMD ["eswrapper"]
# Mon, 26 Jan 2026 22:06:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d182edadba68dca79e806587059ed493f733ae59e4740a44688de1ed388ed655`  
		Last Modified: Mon, 26 Jan 2026 22:07:13 GMT  
		Size: 4.3 MB (4297454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55bdacce276352ebc4d95b2c84ed5d93888b880abfb4114d74af4462f09cdf`  
		Last Modified: Mon, 26 Jan 2026 22:07:13 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c651b3f08321f77950c3adda092d18bdcd0096481325cd6d4640a4eef673d885`  
		Last Modified: Mon, 26 Jan 2026 22:07:13 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db905027beecb3e8feaf15ff16a8bc2c66d41ec76010bc261b677ed7318a70`  
		Last Modified: Mon, 26 Jan 2026 22:07:22 GMT  
		Size: 539.6 MB (539583741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2750bdc748e8dba40e0c63b9a14363c976408fa254d5cb2b5a10671a274457db`  
		Last Modified: Mon, 26 Jan 2026 22:07:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d495e5467649012bc33dff04e6fe73a961af06636119e50b90e83abe31b64`  
		Last Modified: Mon, 26 Jan 2026 22:07:14 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1534fe0701097d535925a211ec110452570691d279566eaf385000eadbb8ab0`  
		Last Modified: Mon, 26 Jan 2026 22:07:14 GMT  
		Size: 74.1 KB (74106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7185b3a3cd0c6a64ad985190d288718ef5df66b7a54a224dfe577b579f60c4ec`  
		Last Modified: Mon, 26 Jan 2026 22:07:15 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8cbcd0da75482e50857010818f1ed0485c37d0c4c348b52f6eec416a29d216e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e5940bb8b88bc7b845ba8603fd9e8dfa07404a760a0b7cacc8024193e4114`

```dockerfile
```

-	Layers:
	-	`sha256:f13656cb08e2493a599d2d235c2072d222e33a4e3fde3c1b66bbaa9b27aa1790`  
		Last Modified: Mon, 26 Jan 2026 22:07:13 GMT  
		Size: 2.1 MB (2098649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b6deae7cbe3cb3bebbb5eb948f3be34ef3e1515f707196830a5cbf60091a71`  
		Last Modified: Mon, 26 Jan 2026 22:07:13 GMT  
		Size: 34.0 KB (34036 bytes)  
		MIME: application/vnd.in-toto+json
