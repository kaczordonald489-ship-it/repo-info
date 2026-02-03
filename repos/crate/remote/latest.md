## `crate:latest`

```console
$ docker pull crate@sha256:b29cb49440c3780e97862409337ce312e9f7a33eeee2ad5b539f229dbb091755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:1ed9696fdb6c192b10b589239ed4de57f02d58bbcb0b9657c3ec71da6fd51694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231666211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0475cdbd4257c115f95849b9a05b7ae9711e12b3cb099624d2c0ddea87090b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:39 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:39 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:42:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:43:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Thu, 29 Jan 2026 18:43:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:43:08 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:43:08 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:43:08 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:43:08 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:43:08 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:43:08 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:43:08 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:43:08 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:43:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Thu, 29 Jan 2026 18:43:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:43:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:43:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c6c90a8e86909827c53164e7490e1dfe1539d2449ad8ba1a4cdc744e87c50cf1`  
		Last Modified: Thu, 29 Jan 2026 18:12:55 GMT  
		Size: 67.5 MB (67497565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d649108e0a1a1e09f818067357225622cd440bf15061bef6344c43041f9d17`  
		Last Modified: Thu, 29 Jan 2026 18:43:27 GMT  
		Size: 13.1 MB (13089656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4db8e76c81f677a4319b3bebc3ba6b4fd7621d09d6ee0e641207ea0e8c407da`  
		Last Modified: Thu, 29 Jan 2026 18:43:29 GMT  
		Size: 149.1 MB (149133497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e662d7966dde5b4c5bcf21b98c55793027a8c6522311630cd684a4aa9ccbd`  
		Last Modified: Thu, 29 Jan 2026 18:43:26 GMT  
		Size: 1.9 MB (1943622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db88dbb600fbbac7c5d7168878cca35155075e9771521ba865279f07d51a17b`  
		Last Modified: Thu, 29 Jan 2026 18:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463e02081b8521c8ac14b2af52fc4bbad6e68574e8912927d1a752e299dc5d1`  
		Last Modified: Thu, 29 Jan 2026 18:43:27 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70406649768f86d0276e003804e36a68357eb8214d43de011eca41517f4480`  
		Last Modified: Thu, 29 Jan 2026 18:43:28 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e28bc57b57015d15b6edc63800b8320de665813a1937ad2786c3e8a61c8b62`  
		Last Modified: Thu, 29 Jan 2026 18:43:28 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:19451facc7ec1a2e9af8b287973c438fc80962a3c894c66864724ab990d9070c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f14865ebd85b2e8d8568e0838708a37e693b3997d9cc897f62b8dc295e398a4`

```dockerfile
```

-	Layers:
	-	`sha256:23ca962f7eb47fd788cf4ca27eb34b50aad8ded47b637c5562e80ef99465c377`  
		Last Modified: Thu, 29 Jan 2026 18:43:26 GMT  
		Size: 5.1 MB (5149317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8aaad692b43ac0f53fc43c984df9c86cb077f21706fb1e178e0f695092648cc`  
		Last Modified: Thu, 29 Jan 2026 18:43:26 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:5a9cde80d459067cec6103f1621eec6f6bcf7db7b7a9fe846d5202ea907e26a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230884959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f77e2fcc2478110c5b4c58bb33619c7d579d52c20dbf9577c3f08725a2a947`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:40 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:40 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:43:21 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:43:35 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.1.2.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.1.2.tar.gz.asc crate-6.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-6.1.2.tar.gz.asc     && tar -xf crate-6.1.2.tar.gz -C /crate --strip-components=1     && rm crate-6.1.2.tar.gz # buildkit
# Thu, 29 Jan 2026 18:43:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:43:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:43:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:43:36 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:43:36 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:43:36 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:43:36 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:43:36 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:43:36 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:43:36 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T14:29:01.562254 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.1.2
# Thu, 29 Jan 2026 18:43:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:43:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:43:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:dc4cc267c74fe1849185ec1aa3a49c7281f8bd96219b60eef2f570ccc68739e3`  
		Last Modified: Thu, 29 Jan 2026 18:12:58 GMT  
		Size: 66.0 MB (65978521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dd915c34ba74327fa17da0d260f2c73ce1defa451356ca4933bffa0f1d202e`  
		Last Modified: Thu, 29 Jan 2026 18:43:55 GMT  
		Size: 13.1 MB (13139064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f683be84365b53773457899dfdfe4e5ba6d86368ca3ed85f6273df12dd48c1`  
		Last Modified: Thu, 29 Jan 2026 18:43:58 GMT  
		Size: 149.8 MB (149821866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e15976b3c1c7de192870ddb7c732ddea02fc89e3920bb547bf99112d1d02843`  
		Last Modified: Thu, 29 Jan 2026 18:43:54 GMT  
		Size: 1.9 MB (1943625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d642b9f8bccb47b98323fce0a481f657572d348d556a8ea97f8c3303bdc0f0f`  
		Last Modified: Thu, 29 Jan 2026 18:43:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a135bfd4999ea88bbe24d47afd75c7c63c984295aa249d20a0196a5bcc4150e5`  
		Last Modified: Thu, 29 Jan 2026 18:43:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc53a578645ad3d193ae8746d6625e6cb648480661d2cf061b8d74dc315bc093`  
		Last Modified: Thu, 29 Jan 2026 18:43:56 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6d46ee7e19c87a3f561566b3bb993835b58eea68eb0924eceb682e045736b6`  
		Last Modified: Thu, 29 Jan 2026 18:43:56 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:b9dac88359f0cb8eb15a609aa5746320ace194ab1d218f56da9e8f1444f60c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd5db7075b2789015ababc3db911d03ae50b27b70db98ac44978b3d560cfd78`

```dockerfile
```

-	Layers:
	-	`sha256:c4801f2edd666c5fb6a20463ca29f894413d4bfa83c7e2df235ece93fb5a9b01`  
		Last Modified: Thu, 29 Jan 2026 18:43:54 GMT  
		Size: 5.1 MB (5147236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b852741dfb3b29e32d80cdc01aaa16e80dc1406e66fa0c6c004626ed4f895687`  
		Last Modified: Thu, 29 Jan 2026 18:43:54 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json
