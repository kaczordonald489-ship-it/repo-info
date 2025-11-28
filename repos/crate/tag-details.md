<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.15`](#crate51015)
-	[`crate:6.0`](#crate60)
-	[`crate:6.0.4`](#crate604)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.1`](#crate611)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:7abd0f53479dea8e8d7a24bc70fe6ccd97d1d7ea41dbd006afa0b94252c3a323
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:1673f62f5140dc0a2efc857503fe9788b520fa8394c646ff5d70d9a149aa3c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233637615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6db51a80547dda346cc3d984359dcf57574b4543cc3d6c48e2f61d6eb93d7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:51:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.15.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.15.tar.gz.asc crate-5.10.15.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.15.tar.gz.asc     && tar -xf crate-5.10.15.tar.gz -C /crate --strip-components=1     && rm crate-5.10.15.tar.gz # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:51:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:51:07 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:51:07 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:51:07 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:51:07 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T10:22:26.338520 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.15
# Mon, 24 Nov 2025 17:51:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:51:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75365895a2605fd43693e4b23e26eebd592768d92b5078e5cbed00c4a689c0de`  
		Last Modified: Mon, 24 Nov 2025 17:51:08 GMT  
		Size: 14.5 MB (14512725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3880ef83ba40dd6163b783358048750e338f42eaba52404def739247f3c2cd7e`  
		Last Modified: Mon, 24 Nov 2025 18:39:04 GMT  
		Size: 149.7 MB (149721615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a6cf02d4c644105ab0ba76555bd210c6bdebbd4190329f68a2dce7143b3a14`  
		Last Modified: Mon, 24 Nov 2025 17:51:33 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a8bc2ae680f5b1cb4300175250d3691d2d489023386712b740d9743c07b48`  
		Last Modified: Mon, 24 Nov 2025 17:51:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449a6c68446388d7dbfca939e949e7662f2077059f6306b6f04a408970a2635`  
		Last Modified: Mon, 24 Nov 2025 17:51:32 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001b6b3b4a483d3504704d754447bc82f633d0b2b8ea474f913589759b732201`  
		Last Modified: Mon, 24 Nov 2025 17:51:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3cd50ce0c599c72aa9b3c24f2f004de620ebe937fec7da7a99d4817778828a`  
		Last Modified: Mon, 24 Nov 2025 17:51:33 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:4fc9e573701dda48d27e2a75d9c661253947234ad51e97b9fcdf61776115087f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584f26b3f1bdaee8306e5ee9e90a05c25614406609a98bd9763e11157ba07c15`

```dockerfile
```

-	Layers:
	-	`sha256:bc65644d023209862b20069374ffabdb96cba4443de43548920a9930f376db27`  
		Last Modified: Mon, 24 Nov 2025 18:38:22 GMT  
		Size: 5.2 MB (5188846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791dae01ad3d4044af0b53114146e3e26f83ce8ddc1096312eb74194f31c2d4f`  
		Last Modified: Mon, 24 Nov 2025 18:38:23 GMT  
		Size: 22.9 KB (22878 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:756c666d149cae8af508b0fa4f66aa6cddf29a1a99ad284dbdefdeedc925e638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232856521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbc53c1d05000d0dcaed8955302830393f55bcc3e0dd8c43c03db8f7412fd0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:25 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:51:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.15.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.15.tar.gz.asc crate-5.10.15.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.15.tar.gz.asc     && tar -xf crate-5.10.15.tar.gz -C /crate --strip-components=1     && rm crate-5.10.15.tar.gz # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:51:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:51:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:51:21 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:51:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:51:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T10:22:26.338520 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.15
# Mon, 24 Nov 2025 17:51:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:51:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ec04509117871c73b2e7290f0eb3cb0beb0c2b6da505f8f8191bf18cc207f`  
		Last Modified: Mon, 24 Nov 2025 17:51:29 GMT  
		Size: 14.6 MB (14567696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bef1137214678baad3887c32c5a5bbb986ed42cfe688c18465ff8b7805484b9`  
		Last Modified: Mon, 24 Nov 2025 22:06:18 GMT  
		Size: 150.4 MB (150400337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367e73df5488d6de8b8a28278b0e491e4dca6d221fcc0155f2693950bcf8ae67`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe01347cebb951fd6fc4e93f327b987efb31fb9af74793fb5bcd7d9142f60a6c`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cb396b5695c1648a03ba6d0f0b5e8fe75bb48eb8aefdf660a6340b21722fd1`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f25f29f80f911b0138ff7c9ebd9298a980eef6c1d593ae72f9c470706d25d7`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65afdff72bdc8c11b2f35d8154828a55e59bf6c1a3c8cdaa4fd702c0c9da250`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:922463e1f176bcc1d76c71653c519aa305121cf5bd055ec02016047e506a166a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e8950f505caa6f6360cb015fb6c41418a9210bcccf168fc8817c15cfb017fb`

```dockerfile
```

-	Layers:
	-	`sha256:ff31e33afb2e987dfef11335adbc9a31023adac09b61f211adc12c70a00594e5`  
		Last Modified: Mon, 24 Nov 2025 18:38:29 GMT  
		Size: 5.2 MB (5186142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004f12d7ab2d53d50bf914951ea66d3cc9528d08287033b57714dc6715fdf132`  
		Last Modified: Mon, 24 Nov 2025 18:38:29 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.15`

```console
$ docker pull crate@sha256:7abd0f53479dea8e8d7a24bc70fe6ccd97d1d7ea41dbd006afa0b94252c3a323
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.15` - linux; amd64

```console
$ docker pull crate@sha256:1673f62f5140dc0a2efc857503fe9788b520fa8394c646ff5d70d9a149aa3c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233637615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6db51a80547dda346cc3d984359dcf57574b4543cc3d6c48e2f61d6eb93d7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:51:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.15.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.15.tar.gz.asc crate-5.10.15.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.15.tar.gz.asc     && tar -xf crate-5.10.15.tar.gz -C /crate --strip-components=1     && rm crate-5.10.15.tar.gz # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:51:07 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:51:07 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:51:07 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:51:07 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:51:07 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T10:22:26.338520 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.15
# Mon, 24 Nov 2025 17:51:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:51:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:51:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75365895a2605fd43693e4b23e26eebd592768d92b5078e5cbed00c4a689c0de`  
		Last Modified: Mon, 24 Nov 2025 17:51:08 GMT  
		Size: 14.5 MB (14512725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3880ef83ba40dd6163b783358048750e338f42eaba52404def739247f3c2cd7e`  
		Last Modified: Mon, 24 Nov 2025 18:39:04 GMT  
		Size: 149.7 MB (149721615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a6cf02d4c644105ab0ba76555bd210c6bdebbd4190329f68a2dce7143b3a14`  
		Last Modified: Mon, 24 Nov 2025 17:51:33 GMT  
		Size: 1.9 MB (1943628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a8bc2ae680f5b1cb4300175250d3691d2d489023386712b740d9743c07b48`  
		Last Modified: Mon, 24 Nov 2025 17:51:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449a6c68446388d7dbfca939e949e7662f2077059f6306b6f04a408970a2635`  
		Last Modified: Mon, 24 Nov 2025 17:51:32 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001b6b3b4a483d3504704d754447bc82f633d0b2b8ea474f913589759b732201`  
		Last Modified: Mon, 24 Nov 2025 17:51:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3cd50ce0c599c72aa9b3c24f2f004de620ebe937fec7da7a99d4817778828a`  
		Last Modified: Mon, 24 Nov 2025 17:51:33 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.15` - unknown; unknown

```console
$ docker pull crate@sha256:4fc9e573701dda48d27e2a75d9c661253947234ad51e97b9fcdf61776115087f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584f26b3f1bdaee8306e5ee9e90a05c25614406609a98bd9763e11157ba07c15`

```dockerfile
```

-	Layers:
	-	`sha256:bc65644d023209862b20069374ffabdb96cba4443de43548920a9930f376db27`  
		Last Modified: Mon, 24 Nov 2025 18:38:22 GMT  
		Size: 5.2 MB (5188846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791dae01ad3d4044af0b53114146e3e26f83ce8ddc1096312eb74194f31c2d4f`  
		Last Modified: Mon, 24 Nov 2025 18:38:23 GMT  
		Size: 22.9 KB (22878 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.15` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:756c666d149cae8af508b0fa4f66aa6cddf29a1a99ad284dbdefdeedc925e638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232856521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbc53c1d05000d0dcaed8955302830393f55bcc3e0dd8c43c03db8f7412fd0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:25 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:51:20 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.15.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.15.tar.gz.asc crate-5.10.15.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.15.tar.gz.asc     && tar -xf crate-5.10.15.tar.gz -C /crate --strip-components=1     && rm crate-5.10.15.tar.gz # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:51:21 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:51:21 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:51:21 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:51:21 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:51:21 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T10:22:26.338520 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.15
# Mon, 24 Nov 2025 17:51:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:51:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:51:21 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ec04509117871c73b2e7290f0eb3cb0beb0c2b6da505f8f8191bf18cc207f`  
		Last Modified: Mon, 24 Nov 2025 17:51:29 GMT  
		Size: 14.6 MB (14567696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bef1137214678baad3887c32c5a5bbb986ed42cfe688c18465ff8b7805484b9`  
		Last Modified: Mon, 24 Nov 2025 22:06:18 GMT  
		Size: 150.4 MB (150400337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367e73df5488d6de8b8a28278b0e491e4dca6d221fcc0155f2693950bcf8ae67`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe01347cebb951fd6fc4e93f327b987efb31fb9af74793fb5bcd7d9142f60a6c`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cb396b5695c1648a03ba6d0f0b5e8fe75bb48eb8aefdf660a6340b21722fd1`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f25f29f80f911b0138ff7c9ebd9298a980eef6c1d593ae72f9c470706d25d7`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65afdff72bdc8c11b2f35d8154828a55e59bf6c1a3c8cdaa4fd702c0c9da250`  
		Last Modified: Mon, 24 Nov 2025 17:51:49 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.15` - unknown; unknown

```console
$ docker pull crate@sha256:922463e1f176bcc1d76c71653c519aa305121cf5bd055ec02016047e506a166a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e8950f505caa6f6360cb015fb6c41418a9210bcccf168fc8817c15cfb017fb`

```dockerfile
```

-	Layers:
	-	`sha256:ff31e33afb2e987dfef11335adbc9a31023adac09b61f211adc12c70a00594e5`  
		Last Modified: Mon, 24 Nov 2025 18:38:29 GMT  
		Size: 5.2 MB (5186142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004f12d7ab2d53d50bf914951ea66d3cc9528d08287033b57714dc6715fdf132`  
		Last Modified: Mon, 24 Nov 2025 18:38:29 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0`

```console
$ docker pull crate@sha256:c956b8894cf7d77e0c436d7ba68ce0a06bd885f3d942387ee7b987af00a175ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:4ec1563fb930c2e1ca9c4efd0169796f4ee1d2f6b75c1d9859169149f752aa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232945497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f583bce06b9b01f5cc3d048dd3301f3222ea05fb99c34aa5a707b3466a135eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:51:30 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:51:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.4.tar.gz.asc crate-6.0.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.4.tar.gz.asc     && tar -xf crate-6.0.4.tar.gz -C /crate --strip-components=1     && rm crate-6.0.4.tar.gz # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:51:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:51:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:51:44 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:51:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:51:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T11:20:09.112895 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.4
# Mon, 24 Nov 2025 17:51:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:51:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369377e9c03f27d0901e141e5d5687eee808535ce5b0edc40d9ad75a2c195d2a`  
		Last Modified: Mon, 24 Nov 2025 17:52:16 GMT  
		Size: 14.5 MB (14512700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd4e849f25435088156248257e4d75700b3e82aa97a61d1a4173e00b0f2e4c`  
		Last Modified: Mon, 24 Nov 2025 22:03:36 GMT  
		Size: 149.0 MB (149029524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea59d141a1a35238332c2c326dc200f84d2f1858e1f8c66f48390f5fe2ffad9d`  
		Last Modified: Mon, 24 Nov 2025 17:52:12 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9281b0333be226e9580134f1d631831700c843afd304d84c7234579d481462`  
		Last Modified: Mon, 24 Nov 2025 17:52:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39b3c2ffc9d307efb4e45de55d00a23c357c43e022d12133cd23c54e04a2fd3`  
		Last Modified: Mon, 24 Nov 2025 17:52:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40909d9c82593431945e2b0587387102fdc82f65abd4853f1d2d13f56df68d61`  
		Last Modified: Mon, 24 Nov 2025 17:52:12 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc0ff6c6ef32054721b8cb507f36ce44b0a176e7a006894414678753a9e5ac9`  
		Last Modified: Mon, 24 Nov 2025 17:52:13 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:4ea6f7c3b1c4adf9577047d800ca13fb832a2e4f771c48761c870f53e96c1700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7def1e4e376e54524afe79eb7be15f05eb870324d1126aeb3fafcc764217c6f0`

```dockerfile
```

-	Layers:
	-	`sha256:17249b1f3b934a9d6c49bfc039cbb968fec1812584ea405c63c9a47f99d6c4ba`  
		Last Modified: Mon, 24 Nov 2025 18:38:31 GMT  
		Size: 5.2 MB (5191984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2990072c7a8ff868d40625139f361ddec648444e1111c9016370ff1c87f74`  
		Last Modified: Mon, 24 Nov 2025 18:38:32 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7abbfa1bedaaaa9e1d1764e47d1686f5bb8090b307a55b2804a9c63327d13adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232173908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ef5421f77fbc1dc65ea2cf1507d5856f953ac59fa5b7753d2fd37e443e737d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:52:15 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:52:28 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.4.tar.gz.asc crate-6.0.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.4.tar.gz.asc     && tar -xf crate-6.0.4.tar.gz -C /crate --strip-components=1     && rm crate-6.0.4.tar.gz # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:52:29 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:52:29 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:52:29 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:52:29 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:52:29 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T11:20:09.112895 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.4
# Mon, 24 Nov 2025 17:52:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:52:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ea6e5523f2a564259b09af92f3140cfe00f71fc3ede1dd53179900a87913bc`  
		Last Modified: Mon, 24 Nov 2025 17:52:58 GMT  
		Size: 14.6 MB (14567793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227fd48a096da14b36f31d6f066cdb133bfb36c9d9e558f88be649268d30b20a`  
		Last Modified: Mon, 24 Nov 2025 17:55:40 GMT  
		Size: 149.7 MB (149717627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc4316babbde5e3febc3ebab08a0b4fe71b4b70e4b8ed3969a4df996c526ebb`  
		Last Modified: Mon, 24 Nov 2025 17:52:57 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee7093be72c21af18a9e6d29d58de86716e8d0141d459b034344a4fdf0084bd`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4badf5441cb763a4f1ba6ae4492726692a3390a9d72d44d5db024aa39f9429`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619718fb6db28dddd0cec88f1fe09e030c17dc798bd4398599045262427c1246`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d53828efb3bdce7ae36f3ba790306652e47055b52030a20109d42884d288c`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:cf4b95a3e7437150b1e75e1b7bf19cc03b8638a3fab0ebc6a80c459fcb5aeef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0bbf6ed67b57bcb59e8bb198dc94956b3230ccedb1cf423aa900cd88856c82`

```dockerfile
```

-	Layers:
	-	`sha256:d85099a8b186641b588daca2eb522f7f319617e8ce0ef6c9112087152c1316d5`  
		Last Modified: Mon, 24 Nov 2025 18:38:37 GMT  
		Size: 5.2 MB (5189891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8f7b122316ee7410fb3f6a4099236e8a9cfc6c39b16860d12261418a781418`  
		Last Modified: Mon, 24 Nov 2025 18:38:37 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.4`

```console
$ docker pull crate@sha256:c956b8894cf7d77e0c436d7ba68ce0a06bd885f3d942387ee7b987af00a175ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.4` - linux; amd64

```console
$ docker pull crate@sha256:4ec1563fb930c2e1ca9c4efd0169796f4ee1d2f6b75c1d9859169149f752aa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232945497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f583bce06b9b01f5cc3d048dd3301f3222ea05fb99c34aa5a707b3466a135eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:51:30 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:51:43 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.4.tar.gz.asc crate-6.0.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.4.tar.gz.asc     && tar -xf crate-6.0.4.tar.gz -C /crate --strip-components=1     && rm crate-6.0.4.tar.gz # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:51:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:51:44 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:51:44 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:51:44 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:51:44 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T11:20:09.112895 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.4
# Mon, 24 Nov 2025 17:51:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:51:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:51:44 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369377e9c03f27d0901e141e5d5687eee808535ce5b0edc40d9ad75a2c195d2a`  
		Last Modified: Mon, 24 Nov 2025 17:52:16 GMT  
		Size: 14.5 MB (14512700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd4e849f25435088156248257e4d75700b3e82aa97a61d1a4173e00b0f2e4c`  
		Last Modified: Mon, 24 Nov 2025 22:03:36 GMT  
		Size: 149.0 MB (149029524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea59d141a1a35238332c2c326dc200f84d2f1858e1f8c66f48390f5fe2ffad9d`  
		Last Modified: Mon, 24 Nov 2025 17:52:12 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9281b0333be226e9580134f1d631831700c843afd304d84c7234579d481462`  
		Last Modified: Mon, 24 Nov 2025 17:52:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39b3c2ffc9d307efb4e45de55d00a23c357c43e022d12133cd23c54e04a2fd3`  
		Last Modified: Mon, 24 Nov 2025 17:52:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40909d9c82593431945e2b0587387102fdc82f65abd4853f1d2d13f56df68d61`  
		Last Modified: Mon, 24 Nov 2025 17:52:12 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc0ff6c6ef32054721b8cb507f36ce44b0a176e7a006894414678753a9e5ac9`  
		Last Modified: Mon, 24 Nov 2025 17:52:13 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.4` - unknown; unknown

```console
$ docker pull crate@sha256:4ea6f7c3b1c4adf9577047d800ca13fb832a2e4f771c48761c870f53e96c1700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7def1e4e376e54524afe79eb7be15f05eb870324d1126aeb3fafcc764217c6f0`

```dockerfile
```

-	Layers:
	-	`sha256:17249b1f3b934a9d6c49bfc039cbb968fec1812584ea405c63c9a47f99d6c4ba`  
		Last Modified: Mon, 24 Nov 2025 18:38:31 GMT  
		Size: 5.2 MB (5191984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2990072c7a8ff868d40625139f361ddec648444e1111c9016370ff1c87f74`  
		Last Modified: Mon, 24 Nov 2025 18:38:32 GMT  
		Size: 22.8 KB (22844 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.4` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:7abbfa1bedaaaa9e1d1764e47d1686f5bb8090b307a55b2804a9c63327d13adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232173908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ef5421f77fbc1dc65ea2cf1507d5856f953ac59fa5b7753d2fd37e443e737d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:52:15 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:52:28 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.4.tar.gz.asc crate-6.0.4.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.4.tar.gz.asc     && tar -xf crate-6.0.4.tar.gz -C /crate --strip-components=1     && rm crate-6.0.4.tar.gz # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:52:29 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:52:29 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:52:29 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:52:29 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:52:29 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T11:20:09.112895 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.4
# Mon, 24 Nov 2025 17:52:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:52:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:52:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ea6e5523f2a564259b09af92f3140cfe00f71fc3ede1dd53179900a87913bc`  
		Last Modified: Mon, 24 Nov 2025 17:52:58 GMT  
		Size: 14.6 MB (14567793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227fd48a096da14b36f31d6f066cdb133bfb36c9d9e558f88be649268d30b20a`  
		Last Modified: Mon, 24 Nov 2025 17:55:40 GMT  
		Size: 149.7 MB (149717627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc4316babbde5e3febc3ebab08a0b4fe71b4b70e4b8ed3969a4df996c526ebb`  
		Last Modified: Mon, 24 Nov 2025 17:52:57 GMT  
		Size: 1.9 MB (1943633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee7093be72c21af18a9e6d29d58de86716e8d0141d459b034344a4fdf0084bd`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4badf5441cb763a4f1ba6ae4492726692a3390a9d72d44d5db024aa39f9429`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619718fb6db28dddd0cec88f1fe09e030c17dc798bd4398599045262427c1246`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d53828efb3bdce7ae36f3ba790306652e47055b52030a20109d42884d288c`  
		Last Modified: Mon, 24 Nov 2025 17:52:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.4` - unknown; unknown

```console
$ docker pull crate@sha256:cf4b95a3e7437150b1e75e1b7bf19cc03b8638a3fab0ebc6a80c459fcb5aeef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0bbf6ed67b57bcb59e8bb198dc94956b3230ccedb1cf423aa900cd88856c82`

```dockerfile
```

-	Layers:
	-	`sha256:d85099a8b186641b588daca2eb522f7f319617e8ce0ef6c9112087152c1316d5`  
		Last Modified: Mon, 24 Nov 2025 18:38:37 GMT  
		Size: 5.2 MB (5189891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8f7b122316ee7410fb3f6a4099236e8a9cfc6c39b16860d12261418a781418`  
		Last Modified: Mon, 24 Nov 2025 18:38:37 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:2c6ced40eaefcdcb196e8a12082ce24ea308152429919486bb521f3474e1fe6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

```console
$ docker pull crate@sha256:9cdbfd5f87ac2e55a01ca14bcea22393cd4f7629fe62e7c3fdaf15a296c9fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233049071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a1eefbe070c18a054f2403a701667ff408bd337e176778801592e97aeef2bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:50:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.1.tar.gz.asc crate-6.1.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.1.tar.gz.asc     && tar -xf crate-6.1.1.tar.gz -C /crate --strip-components=1     && rm crate-6.1.1.tar.gz # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:50:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:50:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:50:27 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:50:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:50:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T12:06:28.986794 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.1
# Mon, 24 Nov 2025 17:50:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:50:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75365895a2605fd43693e4b23e26eebd592768d92b5078e5cbed00c4a689c0de`  
		Last Modified: Mon, 24 Nov 2025 17:51:08 GMT  
		Size: 14.5 MB (14512725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320fdd72b12220a1768084b176c2d643b9e4125fa9af6c4abb4ec454d73d4b2a`  
		Last Modified: Mon, 24 Nov 2025 17:51:38 GMT  
		Size: 149.1 MB (149133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436dbf545d0122c066cc06104cafce85b4923eed1f9d0ecc426c78be5127c11`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b86a3629317251a113d0863f23f343e29ce262b3daf811b4d9526957af8321`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1482b8e25ae0ece7c7da9456017b8dbebbe0e37a09b2985a64926f9635ca9f0`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1e6a635d65cc3e4542f1ae093e7f971ea23ce40be29e3824194bc4582296a`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac4d6f3ef51e3f8326549b07c3a573326a8240d31aaee4292c960a047c10eb0`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:f149dc9199868587908d48b718202dfb4fb4a9e01a353fe966c2892334cbd80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a2919c8364a331ed239117ca5d731f0ed44bc8153425d18840a6ff1e50347c`

```dockerfile
```

-	Layers:
	-	`sha256:3e2a13a467081ce52c24276284efae5b72bb50221d3ce30065e317e6b54b83b1`  
		Last Modified: Mon, 24 Nov 2025 18:38:42 GMT  
		Size: 5.2 MB (5191064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d564f91791778b704cb654ed6c13133d47729d740d413413749ca7b4e8bb49`  
		Last Modified: Mon, 24 Nov 2025 18:38:43 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c9bdd5148d111b114a7e7c5f38ac045d11fb4a8832fd3fe767de1a1d25b265eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232277609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b4ae686df5d0690b99f5c6f5ddf0337a8c4af43041c73a0ccb260e2e16c7cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:25 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:50:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.1.tar.gz.asc crate-6.1.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.1.tar.gz.asc     && tar -xf crate-6.1.1.tar.gz -C /crate --strip-components=1     && rm crate-6.1.1.tar.gz # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:50:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:50:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:50:39 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:50:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:50:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T12:06:28.986794 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.1
# Mon, 24 Nov 2025 17:50:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:50:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ec04509117871c73b2e7290f0eb3cb0beb0c2b6da505f8f8191bf18cc207f`  
		Last Modified: Mon, 24 Nov 2025 17:51:29 GMT  
		Size: 14.6 MB (14567696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e906ad8d2c5bfe2ea09593a677a18fc26a18b5f3fc4e3d3e81c4f3105a2cc`  
		Last Modified: Mon, 24 Nov 2025 17:53:16 GMT  
		Size: 149.8 MB (149821428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4aec223be10183e9888635720d4dd774dc713d776dc663eb5822f43cce024c`  
		Last Modified: Mon, 24 Nov 2025 17:51:28 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7792764d5c4c6c979668e653ebb87d322d70439eff493ef8cc10ce86cfe213`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1307343f3a56da594a0e47f57cd8ec47478d874a38e6b3728362405dc74ac27`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad47ccde51306e41124d56d12e35cd80aedba2e6b548b2ffcb582c6a552fd24`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703907e651f216915026fa62b4a84e90b53bcc8b32bd3ae48ecfed1dfaa05345`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1` - unknown; unknown

```console
$ docker pull crate@sha256:441b13a102a31b5818b83b4d7e05c0e9ac4adfcfb879113b3c218434d8a52510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b827590ae278e8a6d94b0afb2dfe222266f3e9b83d5b6a0be626a114c95578`

```dockerfile
```

-	Layers:
	-	`sha256:77b923e624da0c57724efcb390159a6cb5ef4f10066c54aeaf12f5029e59fc6d`  
		Last Modified: Mon, 24 Nov 2025 18:38:48 GMT  
		Size: 5.2 MB (5188983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b58d599be091b4a9f535f264d0584799dc90f722260798f6d30c6ddb989f507`  
		Last Modified: Mon, 24 Nov 2025 18:38:49 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1.1`

```console
$ docker pull crate@sha256:2c6ced40eaefcdcb196e8a12082ce24ea308152429919486bb521f3474e1fe6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.1` - linux; amd64

```console
$ docker pull crate@sha256:9cdbfd5f87ac2e55a01ca14bcea22393cd4f7629fe62e7c3fdaf15a296c9fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233049071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a1eefbe070c18a054f2403a701667ff408bd337e176778801592e97aeef2bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:50:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.1.tar.gz.asc crate-6.1.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.1.tar.gz.asc     && tar -xf crate-6.1.1.tar.gz -C /crate --strip-components=1     && rm crate-6.1.1.tar.gz # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:50:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:50:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:50:27 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:50:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:50:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T12:06:28.986794 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.1
# Mon, 24 Nov 2025 17:50:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:50:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75365895a2605fd43693e4b23e26eebd592768d92b5078e5cbed00c4a689c0de`  
		Last Modified: Mon, 24 Nov 2025 17:51:08 GMT  
		Size: 14.5 MB (14512725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320fdd72b12220a1768084b176c2d643b9e4125fa9af6c4abb4ec454d73d4b2a`  
		Last Modified: Mon, 24 Nov 2025 17:51:38 GMT  
		Size: 149.1 MB (149133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436dbf545d0122c066cc06104cafce85b4923eed1f9d0ecc426c78be5127c11`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b86a3629317251a113d0863f23f343e29ce262b3daf811b4d9526957af8321`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1482b8e25ae0ece7c7da9456017b8dbebbe0e37a09b2985a64926f9635ca9f0`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1e6a635d65cc3e4542f1ae093e7f971ea23ce40be29e3824194bc4582296a`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac4d6f3ef51e3f8326549b07c3a573326a8240d31aaee4292c960a047c10eb0`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.1` - unknown; unknown

```console
$ docker pull crate@sha256:f149dc9199868587908d48b718202dfb4fb4a9e01a353fe966c2892334cbd80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a2919c8364a331ed239117ca5d731f0ed44bc8153425d18840a6ff1e50347c`

```dockerfile
```

-	Layers:
	-	`sha256:3e2a13a467081ce52c24276284efae5b72bb50221d3ce30065e317e6b54b83b1`  
		Last Modified: Mon, 24 Nov 2025 18:38:42 GMT  
		Size: 5.2 MB (5191064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d564f91791778b704cb654ed6c13133d47729d740d413413749ca7b4e8bb49`  
		Last Modified: Mon, 24 Nov 2025 18:38:43 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.1.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c9bdd5148d111b114a7e7c5f38ac045d11fb4a8832fd3fe767de1a1d25b265eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232277609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b4ae686df5d0690b99f5c6f5ddf0337a8c4af43041c73a0ccb260e2e16c7cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:25 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:50:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.1.tar.gz.asc crate-6.1.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.1.tar.gz.asc     && tar -xf crate-6.1.1.tar.gz -C /crate --strip-components=1     && rm crate-6.1.1.tar.gz # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:50:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:50:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:50:39 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:50:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:50:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T12:06:28.986794 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.1
# Mon, 24 Nov 2025 17:50:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:50:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ec04509117871c73b2e7290f0eb3cb0beb0c2b6da505f8f8191bf18cc207f`  
		Last Modified: Mon, 24 Nov 2025 17:51:29 GMT  
		Size: 14.6 MB (14567696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e906ad8d2c5bfe2ea09593a677a18fc26a18b5f3fc4e3d3e81c4f3105a2cc`  
		Last Modified: Mon, 24 Nov 2025 17:53:16 GMT  
		Size: 149.8 MB (149821428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4aec223be10183e9888635720d4dd774dc713d776dc663eb5822f43cce024c`  
		Last Modified: Mon, 24 Nov 2025 17:51:28 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7792764d5c4c6c979668e653ebb87d322d70439eff493ef8cc10ce86cfe213`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1307343f3a56da594a0e47f57cd8ec47478d874a38e6b3728362405dc74ac27`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad47ccde51306e41124d56d12e35cd80aedba2e6b548b2ffcb582c6a552fd24`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703907e651f216915026fa62b4a84e90b53bcc8b32bd3ae48ecfed1dfaa05345`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.1.1` - unknown; unknown

```console
$ docker pull crate@sha256:441b13a102a31b5818b83b4d7e05c0e9ac4adfcfb879113b3c218434d8a52510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b827590ae278e8a6d94b0afb2dfe222266f3e9b83d5b6a0be626a114c95578`

```dockerfile
```

-	Layers:
	-	`sha256:77b923e624da0c57724efcb390159a6cb5ef4f10066c54aeaf12f5029e59fc6d`  
		Last Modified: Mon, 24 Nov 2025 18:38:48 GMT  
		Size: 5.2 MB (5188983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b58d599be091b4a9f535f264d0584799dc90f722260798f6d30c6ddb989f507`  
		Last Modified: Mon, 24 Nov 2025 18:38:49 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:2c6ced40eaefcdcb196e8a12082ce24ea308152429919486bb521f3474e1fe6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:9cdbfd5f87ac2e55a01ca14bcea22393cd4f7629fe62e7c3fdaf15a296c9fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233049071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a1eefbe070c18a054f2403a701667ff408bd337e176778801592e97aeef2bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:56:34 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:56:34 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:19 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:50:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.1.tar.gz.asc crate-6.1.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.1.tar.gz.asc     && tar -xf crate-6.1.1.tar.gz -C /crate --strip-components=1     && rm crate-6.1.1.tar.gz # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:50:27 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:50:27 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:50:27 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:50:27 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:50:27 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T12:06:28.986794 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.1
# Mon, 24 Nov 2025 17:50:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:50:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:50:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:bf67014a460eefcc2ea9a3e32d93628d2fab7f0098a16700a2a69938d153eee9`  
		Last Modified: Mon, 17 Nov 2025 18:57:36 GMT  
		Size: 67.5 MB (67457776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75365895a2605fd43693e4b23e26eebd592768d92b5078e5cbed00c4a689c0de`  
		Last Modified: Mon, 24 Nov 2025 17:51:08 GMT  
		Size: 14.5 MB (14512725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320fdd72b12220a1768084b176c2d643b9e4125fa9af6c4abb4ec454d73d4b2a`  
		Last Modified: Mon, 24 Nov 2025 17:51:38 GMT  
		Size: 149.1 MB (149133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436dbf545d0122c066cc06104cafce85b4923eed1f9d0ecc426c78be5127c11`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b86a3629317251a113d0863f23f343e29ce262b3daf811b4d9526957af8321`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1482b8e25ae0ece7c7da9456017b8dbebbe0e37a09b2985a64926f9635ca9f0`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1e6a635d65cc3e4542f1ae093e7f971ea23ce40be29e3824194bc4582296a`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac4d6f3ef51e3f8326549b07c3a573326a8240d31aaee4292c960a047c10eb0`  
		Last Modified: Mon, 24 Nov 2025 17:51:06 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:f149dc9199868587908d48b718202dfb4fb4a9e01a353fe966c2892334cbd80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a2919c8364a331ed239117ca5d731f0ed44bc8153425d18840a6ff1e50347c`

```dockerfile
```

-	Layers:
	-	`sha256:3e2a13a467081ce52c24276284efae5b72bb50221d3ce30065e317e6b54b83b1`  
		Last Modified: Mon, 24 Nov 2025 18:38:42 GMT  
		Size: 5.2 MB (5191064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d564f91791778b704cb654ed6c13133d47729d740d413413749ca7b4e8bb49`  
		Last Modified: Mon, 24 Nov 2025 18:38:43 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c9bdd5148d111b114a7e7c5f38ac045d11fb4a8832fd3fe767de1a1d25b265eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232277609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b4ae686df5d0690b99f5c6f5ddf0337a8c4af43041c73a0ccb260e2e16c7cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 17 Nov 2025 18:55:32 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 17 Nov 2025 18:55:32 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 17:50:25 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 24 Nov 2025 17:50:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.1.tar.gz.asc crate-6.1.1.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.1.tar.gz.asc     && tar -xf crate-6.1.1.tar.gz -C /crate --strip-components=1     && rm crate-6.1.1.tar.gz # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 17:50:39 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Nov 2025 17:50:39 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
VOLUME [/data]
# Mon, 24 Nov 2025 17:50:39 GMT
WORKDIR /data
# Mon, 24 Nov 2025 17:50:39 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 24 Nov 2025 17:50:39 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-11-19T12:06:28.986794 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.1
# Mon, 24 Nov 2025 17:50:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 24 Nov 2025 17:50:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Nov 2025 17:50:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:0d102ffa32b996b9ace1ac332db3e1fac4dab769a8600ce40ae00f4598d3ca74`  
		Last Modified: Mon, 17 Nov 2025 18:56:19 GMT  
		Size: 65.9 MB (65942987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ec04509117871c73b2e7290f0eb3cb0beb0c2b6da505f8f8191bf18cc207f`  
		Last Modified: Mon, 24 Nov 2025 17:51:29 GMT  
		Size: 14.6 MB (14567696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e906ad8d2c5bfe2ea09593a677a18fc26a18b5f3fc4e3d3e81c4f3105a2cc`  
		Last Modified: Mon, 24 Nov 2025 17:53:16 GMT  
		Size: 149.8 MB (149821428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4aec223be10183e9888635720d4dd774dc713d776dc663eb5822f43cce024c`  
		Last Modified: Mon, 24 Nov 2025 17:51:28 GMT  
		Size: 1.9 MB (1943632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7792764d5c4c6c979668e653ebb87d322d70439eff493ef8cc10ce86cfe213`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1307343f3a56da594a0e47f57cd8ec47478d874a38e6b3728362405dc74ac27`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad47ccde51306e41124d56d12e35cd80aedba2e6b548b2ffcb582c6a552fd24`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703907e651f216915026fa62b4a84e90b53bcc8b32bd3ae48ecfed1dfaa05345`  
		Last Modified: Mon, 24 Nov 2025 17:51:27 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:441b13a102a31b5818b83b4d7e05c0e9ac4adfcfb879113b3c218434d8a52510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b827590ae278e8a6d94b0afb2dfe222266f3e9b83d5b6a0be626a114c95578`

```dockerfile
```

-	Layers:
	-	`sha256:77b923e624da0c57724efcb390159a6cb5ef4f10066c54aeaf12f5029e59fc6d`  
		Last Modified: Mon, 24 Nov 2025 18:38:48 GMT  
		Size: 5.2 MB (5188983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b58d599be091b4a9f535f264d0584799dc90f722260798f6d30c6ddb989f507`  
		Last Modified: Mon, 24 Nov 2025 18:38:49 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
