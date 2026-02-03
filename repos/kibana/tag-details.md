<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.10`](#kibana81910)
-	[`kibana:9.1.10`](#kibana9110)
-	[`kibana:9.2.4`](#kibana924)

## `kibana:8.19.10`

```console
$ docker pull kibana@sha256:bf71bccbd2e96858ef3e3a3551525f15c58a82ccb2f52b212b57a27bd8db86f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.10` - linux; amd64

```console
$ docker pull kibana@sha256:f4b33a8e7fd4eb7f30eef99f88ac7a6282859c6fa22c5cfcc376b5c62f82ad4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440929098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca95ea32292e68f944fc1f720bcec99d1b1927aa84f02a0f1d8930fa0588930`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Thu, 15 Jan 2026 22:30:02 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 15 Jan 2026 22:30:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
RUN fc-cache -v # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
WORKDIR /usr/share/kibana
# Thu, 15 Jan 2026 22:39:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:39:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:39:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 15 Jan 2026 22:39:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 15 Jan 2026 22:39:13 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 15 Jan 2026 22:39:13 GMT
LABEL org.label-schema.build-date=2026-01-08T21:22:46.611Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6803805478ed373f560b161907994536f4cafef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T21:22:46.611Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6803805478ed373f560b161907994536f4cafef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:39:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 15 Jan 2026 22:39:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 15 Jan 2026 22:39:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b1eabffcf7cbabe97a8f0016c86be2ac1d535d52d736cf34e226593c747b01`  
		Last Modified: Thu, 15 Jan 2026 22:40:11 GMT  
		Size: 9.4 MB (9432839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8894e55e4556970e2b9bf6cf72ea85f6d82eaebcb74ae68f3299988e4874d`  
		Last Modified: Thu, 15 Jan 2026 22:40:18 GMT  
		Size: 385.1 MB (385126540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0d262662be73d762250fd3c2400cd7958731a423bca2ee83a3f0752e407b0`  
		Last Modified: Thu, 15 Jan 2026 22:40:10 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394fc48460e8e9bd15a1ce9c21b1367d22fef97ffad22607d06e75889dd6a38c`  
		Last Modified: Thu, 15 Jan 2026 22:40:11 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a83e2245c5d01687d265da75877f4722e2fe4be011920202354e1bd40ad60`  
		Last Modified: Thu, 15 Jan 2026 22:40:11 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b313b0b17fa53a6d9ed040fafecf22a537028112ae1952909a73999a4b05f`  
		Last Modified: Thu, 15 Jan 2026 22:40:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f7b2e3ea6526dc72585701719671110d7fd61dc1678490d714f43be08cac2`  
		Last Modified: Thu, 15 Jan 2026 22:40:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e68716b1b22fcbcace10fdb78c4bdec3450acca092a5bd016e56fd4d3db519`  
		Last Modified: Thu, 15 Jan 2026 22:40:13 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7286720fc832551fb7f047b4cf3a8ee99c374502cd2fee9790d2341749e30bcb`  
		Last Modified: Thu, 15 Jan 2026 22:40:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f968c1d5590a23ca7714b49d9b70a67aa644a8bd0513d0d77ce4886b0d378189`  
		Last Modified: Thu, 15 Jan 2026 22:40:14 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe913104181aef359465723f7a012bffc86bef3e180f385161e056b42ec4fd2f`  
		Last Modified: Thu, 15 Jan 2026 22:40:14 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.10` - unknown; unknown

```console
$ docker pull kibana@sha256:ef8f5e9f4ca796ab3ba7839d4009764c157b22e412caed8e88ad715caf667fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8504a82c72e1afa4cf64f98c37750339201c91da5f2b7b6fd749276e306f1fde`

```dockerfile
```

-	Layers:
	-	`sha256:7fbc9a55c90ebfdc703ba76f5460e4ff0d928315da5e1adc33180f08d67d891f`  
		Last Modified: Thu, 15 Jan 2026 22:40:10 GMT  
		Size: 4.9 MB (4919875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3856f8ea789516324ab0673d664b191a96f0d9df206eb01452e0bcc83e837745`  
		Last Modified: Thu, 15 Jan 2026 22:40:10 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:452de348001cfc2f23cc586790ff2749cc7125c3056dafb79555290273cbb108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.8 MB (453802317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03063e4180f2cf2902b699f7c814a934f9d94afb2af3ad2aca4397c9a0c0caf1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Thu, 15 Jan 2026 22:32:19 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 15 Jan 2026 22:32:19 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:24 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 15 Jan 2026 22:39:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:39:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
RUN fc-cache -v # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
WORKDIR /usr/share/kibana
# Thu, 15 Jan 2026 22:39:25 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:39:25 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:39:25 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:39:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 15 Jan 2026 22:39:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 15 Jan 2026 22:39:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 15 Jan 2026 22:39:27 GMT
LABEL org.label-schema.build-date=2026-01-08T21:22:46.611Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6803805478ed373f560b161907994536f4cafef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T21:22:46.611Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6803805478ed373f560b161907994536f4cafef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:39:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 15 Jan 2026 22:39:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 15 Jan 2026 22:39:27 GMT
USER 1000
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887bfd3dab63c341235f2310b2f0de104cf47abe15582bee09a26ccf72825307`  
		Last Modified: Thu, 15 Jan 2026 22:40:31 GMT  
		Size: 9.4 MB (9446894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95bea82121def6f659e94a168b2d3578c3662639c2e0e1af1b3cb235a969a3a`  
		Last Modified: Thu, 15 Jan 2026 22:40:41 GMT  
		Size: 398.9 MB (398851773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5210a6c3df4e77c6c34960aa0340797469fa56f0310b088dcacacbec14fa9`  
		Last Modified: Thu, 15 Jan 2026 22:40:31 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14628f389a87888aaeb6be660f76ce62b53dddd2cd716cf1379a1293d07802b6`  
		Last Modified: Thu, 15 Jan 2026 22:40:32 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72028896f066f6d60d9b854656007e083860d9b967b3682aea199a00e73a6a03`  
		Last Modified: Thu, 15 Jan 2026 22:40:32 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b74d011e8a721332c54a4e3c8cd487b4b0f6e8e942f1a684d1bc40d30ee36e5`  
		Last Modified: Thu, 15 Jan 2026 22:40:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5305e0985e4f342be0b93aa061f961cf70b478bf36b6e5c4a6ea6438ac132834`  
		Last Modified: Thu, 15 Jan 2026 22:40:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e24a5e0e735c4bc25f47eda0d2ba23d3f2c1f65c0aaa79fe3af2f9ad463f1`  
		Last Modified: Thu, 15 Jan 2026 22:40:33 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc412c57150973172620afc0ce27cd2c97ed3334a07d3f640876ec18ce7aee7`  
		Last Modified: Thu, 15 Jan 2026 22:40:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0b8604c295f0186a8d0e7c9f1dc2d81a9e06b94ad9dddba049fb9ea7e43e19`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969b63fbb1f9012c56ada40cdc108ee255a385042e4ed698beb3157c73adec32`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.10` - unknown; unknown

```console
$ docker pull kibana@sha256:d2c85daaf81dae2045477187b43b134177a5a9a78c47e5d65560ced09d445222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520622879dd47c5613ed5b45257408198692b37086186aaf92806bd07f527459`

```dockerfile
```

-	Layers:
	-	`sha256:fb06acf56a1fec661a63ef7561301831d91e4b0938a588cab5fee383f6d8e8f0`  
		Last Modified: Thu, 15 Jan 2026 22:40:31 GMT  
		Size: 4.9 MB (4920939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fa3317520fb95a4da8283c6f1a06b6f126b688e389139c3d715b46ba6c9019`  
		Last Modified: Thu, 15 Jan 2026 22:40:31 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.10`

```console
$ docker pull kibana@sha256:5d154b68dba2e0a0caa9829138b4f3580f352c99a609fd6c378c7aa113762ecf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.10` - linux; amd64

```console
$ docker pull kibana@sha256:25a11c764798c8fe1d6286a3b895e8c4cff8a800e331dbc28676a3db20dcc003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441382793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d777bb3313aab3f1668466b6c29094d6f0cd2ead1273429b48e3a94e75fc10d6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 26 Jan 2026 22:07:17 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 26 Jan 2026 22:07:17 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:16:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
RUN fc-cache -v # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
WORKDIR /usr/share/kibana
# Mon, 26 Jan 2026 22:16:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:16:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:16:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:16:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:16:36 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 26 Jan 2026 22:16:36 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 26 Jan 2026 22:16:36 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 26 Jan 2026 22:16:36 GMT
USER 1000
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b608db8a68d2bfe6b7b5f9c30b17e9d0168753be536df5ef3ea832be2acdbea2`  
		Last Modified: Mon, 26 Jan 2026 22:17:38 GMT  
		Size: 19.5 MB (19532080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b925079a510f81aadbbd17793e03bbf6da238ee250cac700b11508d2b0cef7`  
		Last Modified: Mon, 26 Jan 2026 22:17:49 GMT  
		Size: 365.3 MB (365287442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36e530c9051134e2587a03040f7d9d68e31425bcb87f11805b3a89d91db9cf1`  
		Last Modified: Mon, 26 Jan 2026 22:17:37 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6c4a1df6f0e24c90479afeb9c33f27edd7606ce9e346f626de422e8e4d68cb`  
		Last Modified: Mon, 26 Jan 2026 22:17:38 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdcc30720783850a0c6434def66c0a021d16ff8a74b1a3fdb6376cfb89f3360`  
		Last Modified: Mon, 26 Jan 2026 22:17:38 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8060acd7f66c46b7a1fcf68356762b5cff5d546835e0517f827cb025390387ca`  
		Last Modified: Mon, 26 Jan 2026 22:17:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86536da71ae87ac1ec8a3525c919025f5fc4bf35b520817c871c4abccc260562`  
		Last Modified: Mon, 26 Jan 2026 22:17:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f7e0adbfa9e260025784b868a789825f1393de2a9a45807251f11531007b3c`  
		Last Modified: Mon, 26 Jan 2026 22:17:39 GMT  
		Size: 4.7 KB (4744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167728bb28b7a463184153fa6bf908aad73e24eeb9a810bf6e3921591cbde827`  
		Last Modified: Mon, 26 Jan 2026 22:17:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1618ad18f360ca2b74400cc6efba48bc7c7f8448a78f1aca206d7c452994a`  
		Last Modified: Mon, 26 Jan 2026 22:17:40 GMT  
		Size: 74.5 KB (74543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9be7f3b49c1e60a4c797f12eb968e9ad95a4d238e02cdab9a4d3e168ee076ca`  
		Last Modified: Mon, 26 Jan 2026 22:17:40 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0e268f744c9268aedd495d704301c8479a9a4b8d1ba03153940d40e8695a63`  
		Last Modified: Mon, 26 Jan 2026 22:17:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:c4933d950adf4497400c2a112da063ef9007699f6ef146246a307a9c2bd29911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5718277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d84dc664f575fefe7b112081238fc1f29c8194fff9a76d744956b89931805d`

```dockerfile
```

-	Layers:
	-	`sha256:6d2f9fb7ac32f9f0208b41e50310742b1eded5407dd51d7354ed89f64838370a`  
		Last Modified: Mon, 26 Jan 2026 22:17:37 GMT  
		Size: 5.7 MB (5675044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cfcd67081d0db4aa9d0c888df1835b817ce25be2cd23be72851cd75f7c92459`  
		Last Modified: Mon, 26 Jan 2026 22:17:37 GMT  
		Size: 43.2 KB (43233 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:237459dfc13f2089fd174f9c687d62fd2c59f8549bd35751d6d82b4a40796722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453245361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d79caa423b83786af0867cc4b1f81014d66090c1016a96235747133030710b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 26 Jan 2026 22:05:50 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 26 Jan 2026 22:05:50 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:13:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 26 Jan 2026 22:13:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
RUN fc-cache -v # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
WORKDIR /usr/share/kibana
# Mon, 26 Jan 2026 22:13:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:13:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:13:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:13:14 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 26 Jan 2026 22:13:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 26 Jan 2026 22:13:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 26 Jan 2026 22:13:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eafe883ea21b27f7eeecae1cd89ef78d4c5864bccdd6f5c11ae20be7cf9da9`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 19.5 MB (19478425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a02de0b9b50986d3094c2e7e630bf6003fe416beaef1a5110b4ec7698937`  
		Last Modified: Mon, 26 Jan 2026 22:14:24 GMT  
		Size: 379.0 MB (378986588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9955483382ba70c26a1b651b8e8cb7981a29a69cbbbfc71cc7dbe401d768b0b`  
		Last Modified: Mon, 26 Jan 2026 22:14:16 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13679e9df58660b6e4b1671846a54fbe911346e5667ecddad34f5bd1fc34e236`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b28b7f60c03f1fc9debf7bfc620dec2b63cafeb3989f24dc6dc07fa35293ce`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1e0f8205e8e4d520cdc51fa70c3fa42ff064b61109796ce039574313f04d6d`  
		Last Modified: Mon, 26 Jan 2026 22:14:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c3efd728184072f97bf634dffaac4227807285f1387b23920078f4fd756c1e`  
		Last Modified: Mon, 26 Jan 2026 22:14:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0d032c19ae2096a83468af119b4bffe065c3750bf61ccf4e6f166d3834238`  
		Last Modified: Mon, 26 Jan 2026 22:14:18 GMT  
		Size: 4.7 KB (4744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477b2c6f544d9245f0d20d55ed840be26dc492156ef9b170e754aef391b4f613`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad30dbea184fd531a034262e0db758197224d8089cae3194e0d9b6d6d04e4dd`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77e5d68122e972fd5f487bf45a77dffb00747769bcbf61c58bc6b98e75419b0`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f75916cde2ed0773f7231d0f03271cb03d2b8938e50f2b0a9ca05d3541d065`  
		Last Modified: Mon, 26 Jan 2026 22:14:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:74584c9f0ca0734aef6b04469f3db6f47a3c0b61d6dbadd592482891e363e337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f255a0b6b0e98cd5a3ef516437d7c6cd83acf21f9f0327cdcf42fc94ac0be62d`

```dockerfile
```

-	Layers:
	-	`sha256:2f46490b59f6c6a0e058791354e70c12449085eb918ff27af55b78192d442263`  
		Last Modified: Mon, 26 Jan 2026 22:14:16 GMT  
		Size: 5.7 MB (5673716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87b34ea18e3e7bf1a67ece86d8670d03ce7170e880cf08ce8553cb220cfc56e1`  
		Last Modified: Mon, 26 Jan 2026 22:14:16 GMT  
		Size: 43.5 KB (43490 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.4`

```console
$ docker pull kibana@sha256:6314ad113eedb82a278335cec7fb79d4104a7a5220a35ce630cd4a23e4305806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.4` - linux; amd64

```console
$ docker pull kibana@sha256:1406af5c908409cdef33bcc10270dc03324e8c3d550919916c326afd3818d2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.4 MB (447442949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0c62eed71bbb29e6791fe40861f0f9516eea6a00fc4f8cd4378eb36182b7dd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 26 Jan 2026 22:08:22 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 26 Jan 2026 22:08:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:17:31 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 26 Jan 2026 22:17:32 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:17:32 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 26 Jan 2026 22:17:32 GMT
RUN fc-cache -v # buildkit
# Mon, 26 Jan 2026 22:17:32 GMT
WORKDIR /usr/share/kibana
# Mon, 26 Jan 2026 22:17:32 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 26 Jan 2026 22:17:32 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:17:32 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:17:32 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 26 Jan 2026 22:17:32 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:17:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 26 Jan 2026 22:17:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 26 Jan 2026 22:17:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 26 Jan 2026 22:17:34 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Mon, 26 Jan 2026 22:17:34 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 26 Jan 2026 22:17:34 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:17:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 26 Jan 2026 22:17:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 26 Jan 2026 22:17:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b506ef00669978cf957d8533abd37a8757cd23ec92134dc2ecc3f112d6d2ccc`  
		Last Modified: Mon, 26 Jan 2026 22:18:32 GMT  
		Size: 19.5 MB (19532103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebad2344c2a402cc351024fdfa030462ce118e5aa08aecd2e966043cf28eb06`  
		Last Modified: Mon, 26 Jan 2026 22:18:41 GMT  
		Size: 371.3 MB (371347436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fdaa1e054a229673fd4449b98d8f8480ff2f4be3892e905acd8d868bdaa4d8`  
		Last Modified: Mon, 26 Jan 2026 22:18:31 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f888e6839a1c2845f0e120f6f812cf3f71c8bad959af713c56c2f53f5263781c`  
		Last Modified: Mon, 26 Jan 2026 22:18:32 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95bdff717f923b623fa1e7e84bdf2c9692dae47b281f89cafdcd023c6e267fc`  
		Last Modified: Mon, 26 Jan 2026 22:18:32 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03843ef985a41ce31982ebfbe480fc10c1269b8fb75018d17f6f577f3a2af03`  
		Last Modified: Mon, 26 Jan 2026 22:18:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baa321bab8c4bf667d34a5dcd6b7d5f054e2c9299347b529ec7b2cd9770d1a7`  
		Last Modified: Mon, 26 Jan 2026 22:18:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d354dc4820202d22ed851d8b15269e2763ccf404ab97a0da733af91d7e784186`  
		Last Modified: Mon, 26 Jan 2026 22:18:34 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77369081c894ffeb7d2d3c6049839c79c7286af273c2280c3a4bda5e7c85fe`  
		Last Modified: Mon, 26 Jan 2026 22:18:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d8b7c0c16ca62b8f832cd4716d90a6b5a5f1f7ec04497cf992c1d9e176ff62`  
		Last Modified: Mon, 26 Jan 2026 22:18:35 GMT  
		Size: 74.5 KB (74542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd3013384c652c24b3db6562186fd3078f61e17d2a7dd96e07522dd593c200d`  
		Last Modified: Mon, 26 Jan 2026 22:18:35 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af24075abde3ae3de30e1f9d673ca1ffa97970a1b8e65b171f9b7792fc9af5`  
		Last Modified: Mon, 26 Jan 2026 22:18:36 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:d3cccf397037ef00dcdc14b735ea7ee4f09b75b9acac1cce383046f6cae23ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b377be354d0b5bbc70e2fbb93270c74bd4a895895dacffbbd47c667385e58d7`

```dockerfile
```

-	Layers:
	-	`sha256:474ab39d3877838b95df2c0a0668b67e724721a398fe2bf159053db4c9137daa`  
		Last Modified: Mon, 26 Jan 2026 22:18:32 GMT  
		Size: 5.8 MB (5750299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e733428a163217bef28a73e1275c43e76c21f3df3d7e116afe50c6b62748f99`  
		Last Modified: Mon, 26 Jan 2026 22:18:31 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1ead890ec301c689870b34112d239ce7c6bda69b5471edb89f8ea9d00d1e9136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.4 MB (459361050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c740bcc91e9cb3c3185e228791b8554e96869e2271962d14bd6744530904e7f6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 26 Jan 2026 22:05:53 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 26 Jan 2026 22:05:53 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:13:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 26 Jan 2026 22:13:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:13:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 26 Jan 2026 22:13:27 GMT
RUN fc-cache -v # buildkit
# Mon, 26 Jan 2026 22:13:27 GMT
WORKDIR /usr/share/kibana
# Mon, 26 Jan 2026 22:13:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 26 Jan 2026 22:13:27 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:13:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:13:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 26 Jan 2026 22:13:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 26 Jan 2026 22:13:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 26 Jan 2026 22:13:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 26 Jan 2026 22:13:29 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Mon, 26 Jan 2026 22:13:29 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 26 Jan 2026 22:13:29 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:13:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 26 Jan 2026 22:13:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 26 Jan 2026 22:13:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e073eaaadb125f3309f3db81de8f63aaa3b6fbcd08606c4216d5d7a1c79f21d`  
		Last Modified: Mon, 26 Jan 2026 22:14:34 GMT  
		Size: 19.5 MB (19478480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262de80465dbc258c602c30ec4e36b3c9c3469586926ac6b2154c95e7dc5e2d3`  
		Last Modified: Mon, 26 Jan 2026 22:14:51 GMT  
		Size: 385.1 MB (385102068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515fbfd48846458d3f1a52f69bfc2c416f1c01c50b60a93b608b5e97f73e4d67`  
		Last Modified: Mon, 26 Jan 2026 22:14:32 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04d97eeb49250d4df14ea9222c8e0e09a28b307296680b4574b658be2a19b01`  
		Last Modified: Mon, 26 Jan 2026 22:14:34 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a04027dc3e4155d6a0edee2c4dce58200995880bb7cfc8e900884154ac9e9b`  
		Last Modified: Mon, 26 Jan 2026 22:14:34 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8c468ce8d08002f3f660d3b184426988dbc0d6257ef9584da0675eabf0312d`  
		Last Modified: Mon, 26 Jan 2026 22:14:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768f3acf0bbc7011acc370ee9a0a92ee4a1c6f6517a3ef55c805c302247e8a73`  
		Last Modified: Mon, 26 Jan 2026 22:14:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8334c0f3de0faba9b83a6d264e5136ef172a15cbf541a14cda19ab2702e55610`  
		Last Modified: Mon, 26 Jan 2026 22:14:35 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4048d9d73fa468bee7154a2441060aac474247266d5ec302727ed2de46b4fdd`  
		Last Modified: Mon, 26 Jan 2026 22:14:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f75ac2b26476e50950de0970dcbafd107028c0514df4ab6b244401850ad2f40`  
		Last Modified: Mon, 26 Jan 2026 22:14:37 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9524f73dbce66e1909deb2acc4070e44998b8fdf72b963e989a351221583a363`  
		Last Modified: Mon, 26 Jan 2026 22:14:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3133cfce9d107fac00ccd39bcbeb5ac4a44dcb955cb35dfce98aa780def59e0c`  
		Last Modified: Mon, 26 Jan 2026 22:14:38 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:d4cd1d85730b5b2d306135067f2b6ce51f3c4323e798108f1be8448682aeffb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de1526a4081d404d3886157f2c3486067e956a5d6db200d9f3cf9553a977704`

```dockerfile
```

-	Layers:
	-	`sha256:6be598ed03323ab308c1d5c6e56bc04e95d3ba90296c20a9acbd72e57ce19677`  
		Last Modified: Mon, 26 Jan 2026 22:14:33 GMT  
		Size: 5.7 MB (5748971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82955a43c4721f8c8751501f6f0cffca0f6786e70058fef23d84b7aaf4e6e171`  
		Last Modified: Mon, 26 Jan 2026 22:14:32 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
