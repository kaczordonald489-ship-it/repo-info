<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.10`](#logstash81910)
-	[`logstash:9.1.10`](#logstash9110)
-	[`logstash:9.2.4`](#logstash924)

## `logstash:8.19.10`

```console
$ docker pull logstash@sha256:555e8dadf9ad013dfd2fdd7e71d7b478074a80edd86822c2fa079b84883847e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.10` - linux; amd64

```console
$ docker pull logstash@sha256:7b953ad28867b5ba54523ac4abc25b07970b3d6beb9c2fdd737452335c542af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.4 MB (521445846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41608b84701fc16a2041abb8c6c4693f8ae45db2c1fd20c717174e369805bbc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 15 Jan 2026 22:31:23 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 15 Jan 2026 22:31:23 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
WORKDIR /usr/share/logstash
# Thu, 15 Jan 2026 22:32:04 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:32:04 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:32:04 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:32:04 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 15 Jan 2026 22:32:04 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 15 Jan 2026 22:32:05 GMT
USER 1000
# Thu, 15 Jan 2026 22:32:05 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 15 Jan 2026 22:32:05 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.10 org.opencontainers.image.version=8.19.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-07T17:24:23+00:00 org.opencontainers.image.created=2026-01-07T17:24:23+00:00
# Thu, 15 Jan 2026 22:32:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106ff9c60e3b0c5caf9876f75b0e7310b18887ab073d5b6c254b6e51484e3765`  
		Last Modified: Thu, 15 Jan 2026 22:32:42 GMT  
		Size: 49.8 MB (49811886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a75ed7773cbf70823ab6f16214f069c73a448c56e85b629af42ccca888f332e`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c116f452c2b93845c457613af44b5bec51a6716e842c2c8344d60a6cea88da1d`  
		Last Modified: Thu, 15 Jan 2026 22:32:49 GMT  
		Size: 441.6 MB (441640221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e55bbed2aef1fa6dc69dee5568808f3cc413ab6bd97be2783c0142469d0b0`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0740e857072ed647e436c435e397b2b1325d2ece9b013b3c33d804d78cb4e`  
		Last Modified: Thu, 15 Jan 2026 22:32:40 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaee70b78cf97de53ab844f5847ecf41806aea1795fa4c32caedd0205c6c233`  
		Last Modified: Thu, 15 Jan 2026 22:32:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20401eda2953ef0b0ead602de4b6255b5cb4d43dd0242c34099ea4dca2d4d9ee`  
		Last Modified: Thu, 15 Jan 2026 22:32:42 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5a1de0bed25db992ea94b99e45fb796bf4d4a0ea21c7a71446f2ead25d42dd`  
		Last Modified: Thu, 15 Jan 2026 22:32:42 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be2883b856b67a053014231e409532dc327b15369bead35116ac7dad522e23b`  
		Last Modified: Thu, 15 Jan 2026 22:32:43 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cac1d1d0771b591c0e22f728b3c3b6372e540e23a818bbb3ab6a184a2be844`  
		Last Modified: Thu, 15 Jan 2026 22:32:43 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417ef8ab86e54a79dec82445546991485365e8ea978094c1728767e4e7ffc2b2`  
		Last Modified: Thu, 15 Jan 2026 22:32:43 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.10` - unknown; unknown

```console
$ docker pull logstash@sha256:23be666d31cd06d5b49345ed65138200dc2d1149ac89ae387ce9a543cf356b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20e2c5bffc3cf590f6a8b7f8c0ef303bd67864904b8d34e4bb6759db54385c8`

```dockerfile
```

-	Layers:
	-	`sha256:f054f1846362af1924cf04b0fc62923d8c6c168aa71248b4f28a15a6b38d532d`  
		Last Modified: Thu, 15 Jan 2026 22:32:40 GMT  
		Size: 3.7 MB (3651746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf40b739af4bd5f782971edd51cd904f0028d40ea7acffb0dea322561fc3f9ec`  
		Last Modified: Thu, 15 Jan 2026 22:32:39 GMT  
		Size: 35.8 KB (35844 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:dc292a7be44ad6b4403195e37d5b0beaecb19ea81ede8f9ff73b8d84e8d34db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.1 MB (521121894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c13ffd3c2cdcee2ea46e59d39e95457336163d0cfb996bbd2c0c1c9fe5941c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Thu, 15 Jan 2026 22:33:28 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 15 Jan 2026 22:33:28 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.10-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.10 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
WORKDIR /usr/share/logstash
# Thu, 15 Jan 2026 22:34:11 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:34:11 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:34:11 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:34:12 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
USER 1000
# Thu, 15 Jan 2026 22:34:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 15 Jan 2026 22:34:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.10 org.opencontainers.image.version=8.19.10 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-01-07T17:24:23+00:00 org.opencontainers.image.created=2026-01-07T17:24:23+00:00
# Thu, 15 Jan 2026 22:34:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78c15fc0b37d907e3bb93005da18e1c66d8c7f5ce81ec7adc4cbf1f453923e`  
		Last Modified: Thu, 15 Jan 2026 22:34:52 GMT  
		Size: 52.1 MB (52065432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d7bcac2f41a34a4e6da98b8f3af1305316671dd8dfa5528cc81a608686d65a`  
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9846089205883a9e4c376f9b125e71f7eeee2ef25910211f37152150b0a652`  
		Last Modified: Thu, 15 Jan 2026 22:35:00 GMT  
		Size: 439.9 MB (439924907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0b366a472f185bd2a11956165160bb3f460a2c3e440087b1c6837170cd4260`  
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14936df0f6a23e4429128c2a1b1432d1ad70b48b53fb617d2c4e92374f3523b`  
		Last Modified: Thu, 15 Jan 2026 22:34:51 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d74cb030ea7e313e8cd7a0ed66c22c26370442c070dde06d5b7a9a526fc008`  
		Last Modified: Thu, 15 Jan 2026 22:34:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d699a4f40f9e4169b2941e11a512305fe497924f849469ec9f6f074e853eba`  
		Last Modified: Thu, 15 Jan 2026 22:34:52 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee59793887602ab2816f376a5174af463b8192bad06c347f60f7b53718896bf2`  
		Last Modified: Thu, 15 Jan 2026 22:34:52 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec084120a0a5d3867ad36240eed627b971ebab6cbe9ec89caf2ba49cf02e844e`  
		Last Modified: Thu, 15 Jan 2026 22:34:53 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51d0d79ab269e9945110621d4da0c32fea5cb60a68d0940ff2991224f1db33`  
		Last Modified: Thu, 15 Jan 2026 22:34:53 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b22e41bf5db741511ee69eeea3bf419b6a1c8a7467ed8a1e47ec6e4db89f5d`  
		Last Modified: Thu, 15 Jan 2026 22:34:54 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.10` - unknown; unknown

```console
$ docker pull logstash@sha256:8872adf5a502a162012c618e93c48a159f4d74fe380a5dd6dcdfc69ac3e18c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3245f4bbea9e8bb1c09b8675d6ba84d3433d6e39b2a17f4bf78340b6ef44d91c`

```dockerfile
```

-	Layers:
	-	`sha256:e492d2475306c543c8d15ad77c572cf19b4ba7c65b98649256f09398500f74e7`  
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
		Size: 3.7 MB (3652171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9636c18161852dc6094863744875e4fa85977c8d6767aea42d4b81755c8b4b9`  
		Last Modified: Thu, 15 Jan 2026 22:34:49 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.10`

```console
$ docker pull logstash@sha256:c6c8d932806bb685ed60bd1309e77c8f66aa41c2ee6aeccd2113b7c74f2e2337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.10` - linux; amd64

```console
$ docker pull logstash@sha256:bf26ecc3ca6c1cec655589c97361be9e1db8fa542a893f1b9b8497b1d64e8ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.0 MB (475999324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15391406e206d3f2ef245d5f252ad5f6f4ea53d575070841b5be7a43e8818c2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Mon, 26 Jan 2026 22:08:25 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:08:25 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:08:25 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Jan 2026 22:08:25 GMT
WORKDIR /usr/share
# Mon, 26 Jan 2026 22:08:27 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:09:00 GMT
WORKDIR /usr/share/logstash
# Mon, 26 Jan 2026 22:09:00 GMT
USER 1000
# Mon, 26 Jan 2026 22:09:00 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 26 Jan 2026 22:09:00 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 26 Jan 2026 22:09:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f2014f0223687361cc12a7455f1058fdd0eedf18cae7bb514a09d3410e0692`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 5.2 MB (5157710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53de0a38b7b65bd5230bcf26f521bb9e202baaf8f358c11e1e2803d771cc8a4e`  
		Last Modified: Mon, 26 Jan 2026 22:09:41 GMT  
		Size: 430.6 MB (430571860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d22cd9bbcf7e8c0ac1a3262cbc835483f0be26c8b74a9ec3b156088ca2924a`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cc78e5b9eadac8bb1a5992a99e3d2038de133183d40f7f17f6f5589bc3ddb2`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7046d989e43b957a9f0297c413c47b5fd57dcee04ff77d6cbdfebb42b3be9e6`  
		Last Modified: Mon, 26 Jan 2026 22:09:34 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe8eb55c57ee7ed56d186e50dd7b035f7d26088f91aa2015d2b127fdf6b961b`  
		Last Modified: Mon, 26 Jan 2026 22:09:34 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb04f99cac0a2de36b3cca7b627c0832b13e8654dd11bdf531edfc6480962cf6`  
		Last Modified: Mon, 26 Jan 2026 22:09:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7005ff28fafa6181f3190ae3bb94a2af2eee2bf77901f79af105829292b95`  
		Last Modified: Mon, 26 Jan 2026 22:09:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62cfff653b1ac5b44f4d3a4f51e11207fe45cdbe2a55b1d3e711ede72e990a9`  
		Last Modified: Mon, 26 Jan 2026 22:09:36 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:bb32e5d36a31c201c507f6b545e90a2062ffcfc5513876493d57bc422c542c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4a89d8d1c96b1ff5a72ec6dd770e1bfcc2c65079b5f923ccb37ea19736f0a8`

```dockerfile
```

-	Layers:
	-	`sha256:a1250185d79340e5530a8ec9ebf383d51e5d5daf3ab17878c60da5f2a9df9f4d`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 2.1 MB (2088545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904a7d143426dc236d4b35454834071b4f84bc7e492fc29ba498a7989a61ca17`  
		Last Modified: Mon, 26 Jan 2026 22:09:33 GMT  
		Size: 30.2 KB (30164 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.10` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5ef67eac7d2b2baa9c99e6a93fc1e1d9304ef9cf9e469bca909fd27bc6de0ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.5 MB (472493714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e212ffcb3ff49445acd07e89b5798f0b4655aec29a920f5f2f460b42fd7e29e2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Mon, 26 Jan 2026 22:07:35 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:07:35 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:35 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Jan 2026 22:07:35 GMT
WORKDIR /usr/share
# Mon, 26 Jan 2026 22:07:37 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.10-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.10 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 26 Jan 2026 22:08:25 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 26 Jan 2026 22:08:25 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:08:25 GMT
WORKDIR /usr/share/logstash
# Mon, 26 Jan 2026 22:08:25 GMT
USER 1000
# Mon, 26 Jan 2026 22:08:25 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 26 Jan 2026 22:08:25 GMT
LABEL org.label-schema.build-date=2026-01-07T17:17:31+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-07T17:17:31+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 26 Jan 2026 22:08:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adc5ed1a1becf097a6f22cd91cf266fb9cc3985a5805caba78518dffe1893c4`  
		Last Modified: Mon, 26 Jan 2026 22:09:01 GMT  
		Size: 5.2 MB (5155555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ac5fcb2e5372554e33c0519877f40cbe239aaa074b25b5c3a5bf6b2f3927d`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 428.8 MB (428849789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58edc2b0049a542f7acb2574e41b18ccba5bd8d86e5f6e8f199a310d00417d0c`  
		Last Modified: Mon, 26 Jan 2026 22:09:00 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e8b33e821e98bcea55269cc36c395cb4c837f6d85954388da85dae02423e0`  
		Last Modified: Mon, 26 Jan 2026 22:09:00 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80234afe49e28bc2b0a6a16f2b32305516dc96741c99588643051a748499353f`  
		Last Modified: Mon, 26 Jan 2026 22:09:02 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af078debe94f51318b4719124199557892e9289258258f3ac0aad1c00be3921d`  
		Last Modified: Mon, 26 Jan 2026 22:09:02 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8ebb81b172309fec2f24211539d78e550845947c411bfd7a6bc599c8d9a95c`  
		Last Modified: Mon, 26 Jan 2026 22:09:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835d9a5666e7bf2712e0b4810c3c43e2b10c7e58f8c2cc3dbedc8c41caa94e39`  
		Last Modified: Mon, 26 Jan 2026 22:09:03 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27976b6f1397455da9032db32d9e7919400b0a47b16ad0eac4f14e7317f438eb`  
		Last Modified: Mon, 26 Jan 2026 22:09:03 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.10` - unknown; unknown

```console
$ docker pull logstash@sha256:7adceb11ee4334fc0e3e23c84d2954b40131b6fded58af0f45753eeda12b488b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44819da42498f2b42e49c1e57406ddab958fbc41ff0e2716a59c65b7016f4758`

```dockerfile
```

-	Layers:
	-	`sha256:7ec00180d2a0f1b50f9112a221f18b5b9b888b4944f439de156777f48028a7a5`  
		Last Modified: Mon, 26 Jan 2026 22:09:01 GMT  
		Size: 2.1 MB (2089115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1e57d8ff4a6d2931cd5824ec9b72ed24b1ee8cd9cf564bb81332ded41fd9d1`  
		Last Modified: Mon, 26 Jan 2026 22:09:00 GMT  
		Size: 30.2 KB (30241 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.4`

```console
$ docker pull logstash@sha256:a85af62c1c127b74de27ee9fd29796ca67d16513096fbb38eda90350e9cf4e2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.4` - linux; amd64

```console
$ docker pull logstash@sha256:76cbf447bc7c5b896bc7012b19e4a0341dfbc7c9f9feec665303c506228c00ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486306117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039d9ede53a19f513f4415e6b00ad36364ee8cca494c749b44325b4e1e3ec01a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Mon, 26 Jan 2026 22:08:20 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:08:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:08:20 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Jan 2026 22:08:20 GMT
WORKDIR /usr/share
# Mon, 26 Jan 2026 22:08:22 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:09:09 GMT
WORKDIR /usr/share/logstash
# Mon, 26 Jan 2026 22:09:09 GMT
USER 1000
# Mon, 26 Jan 2026 22:09:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 26 Jan 2026 22:09:09 GMT
LABEL org.label-schema.build-date=2026-01-07T21:31:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-07T21:31:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 26 Jan 2026 22:09:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1697809a01ef7c3d99633efe66e7fa021327537c95bd35cbc6d8c3e7e9e7e3a1`  
		Last Modified: Mon, 26 Jan 2026 22:09:44 GMT  
		Size: 5.2 MB (5157734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68729e681a294d51225e241d82a7572fe5fc70795c16904342c439d29149b98`  
		Last Modified: Mon, 26 Jan 2026 22:09:53 GMT  
		Size: 440.9 MB (440878618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ea5bd076e2475796059d6b536d781424c669020f663ef4c04db35b432d3a1e`  
		Last Modified: Mon, 26 Jan 2026 22:09:44 GMT  
		Size: 6.3 KB (6301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd900674574c90849da15d951b7f606d9a20b9d8db2e3d317b01724a595cbb4`  
		Last Modified: Mon, 26 Jan 2026 22:09:44 GMT  
		Size: 255.2 KB (255188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7528740d66abcee19f381ea33113223909799d930df780f90a925dad00000c5`  
		Last Modified: Mon, 26 Jan 2026 22:09:45 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65949e7401063d177f5fdea9c1f4fb111a0c7b515dd62676750ebca4d4df52d3`  
		Last Modified: Mon, 26 Jan 2026 22:09:45 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e303704d02a990feaf2555bbf9dc66140e3a847812c27f2b02f24a6fd314b018`  
		Last Modified: Mon, 26 Jan 2026 22:09:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4924a4a4eb958b65d0248cfbed1bc3a0d8890aaa48ec3d5a5cf04132394773`  
		Last Modified: Mon, 26 Jan 2026 22:09:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af64df66a4b136eb2f5e08d2844e9e1ca02a3896144c7681a9dcd6ecf72d3b58`  
		Last Modified: Mon, 26 Jan 2026 22:09:47 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.4` - unknown; unknown

```console
$ docker pull logstash@sha256:c6ad5eb7683430c70637e6b713e3dc646f14ce85a36d385cd679a4e43f361507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2128559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a44043307361a9d8fdcb3d169eee15e549735af0264138e982dd1b2d5203c63`

```dockerfile
```

-	Layers:
	-	`sha256:1c474eb9d810f7da4c1dfe0005c1e7d4f7249b97dc53292ce254d265df7f107e`  
		Last Modified: Mon, 26 Jan 2026 22:09:44 GMT  
		Size: 2.1 MB (2098360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d441205987ed9511b9cffb94fa7eb1560f6f5f4c071881b6db5fc2322dfc44e9`  
		Last Modified: Mon, 26 Jan 2026 22:09:44 GMT  
		Size: 30.2 KB (30199 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:625da7af4dd7ceaf7261893cb4a4ac9a7373e7b6a732d159c9e32ddb44313e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.8 MB (482800391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3a84ddd73e26b9ce6db1f467666932cc289d8becbac63433a72b9b25eb9334`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

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
# Mon, 26 Jan 2026 22:07:54 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:07:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:54 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Jan 2026 22:07:54 GMT
WORKDIR /usr/share
# Mon, 26 Jan 2026 22:07:56 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:08:44 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.4-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.4 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 26 Jan 2026 22:08:44 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 26 Jan 2026 22:08:45 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 26 Jan 2026 22:08:45 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 26 Jan 2026 22:08:45 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 26 Jan 2026 22:08:45 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 26 Jan 2026 22:08:45 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 26 Jan 2026 22:08:45 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:08:45 GMT
WORKDIR /usr/share/logstash
# Mon, 26 Jan 2026 22:08:45 GMT
USER 1000
# Mon, 26 Jan 2026 22:08:45 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 26 Jan 2026 22:08:45 GMT
LABEL org.label-schema.build-date=2026-01-07T21:31:02+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-07T21:31:02+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 26 Jan 2026 22:08:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfd1a216bc0a996f76e86e1fd2046d76d23014967a8049c7bb3a365efec239d`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 5.2 MB (5155455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d212b905fe75d943f74b671ef9cac24660e412d6755a10a04fd330b15938dc`  
		Last Modified: Mon, 26 Jan 2026 22:09:31 GMT  
		Size: 439.2 MB (439156553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e4b735b3670a40092676fa6cf406b7012b64d911afafc666c86e9a7d993399`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff91f9e91374a28eba17374d2c77b21c7b7c382faef8de4d004bf9cc2d256d4`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 255.2 KB (255191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad8ab126e9d3e4bd8a077db274ad8b8ddffa8199c50911a2b449df296dad09e`  
		Last Modified: Mon, 26 Jan 2026 22:09:23 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c02b7e7e78fb55de430eb8540e4e300e1f86e267dc013951d8deca49d46c550`  
		Last Modified: Mon, 26 Jan 2026 22:09:24 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6b02ca108c20520ff338e627534d42dfc7d64db689a26886c690641447dd76`  
		Last Modified: Mon, 26 Jan 2026 22:09:24 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0113153d29d51e764a09fdc76a337fad5755673e080578dc71636384dd087b1`  
		Last Modified: Mon, 26 Jan 2026 22:09:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34285ced25054c0b09225d4961881f722fbf0ce3f04fb451bfd2ed2e5f399657`  
		Last Modified: Mon, 26 Jan 2026 22:09:25 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.4` - unknown; unknown

```console
$ docker pull logstash@sha256:f346637b6c03b2d91e83130864e1085df8829e49b1e4221042c3fa886549e441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca27952bc403087d1b7690c82a61792bf5a8d7a09465b28babe1d1b4dae8eea`

```dockerfile
```

-	Layers:
	-	`sha256:626767716082b1f979b65e77471fbdf8fd3927ae4152680526648bfa3dd0bcbc`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 2.1 MB (2098930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63776e17aa3e3a2e83b2a6369c8d9c8109e6cb355ee6ca6b6a4763d2e587223f`  
		Last Modified: Mon, 26 Jan 2026 22:09:21 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
