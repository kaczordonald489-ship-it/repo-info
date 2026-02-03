<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.16`](#crate51016)
-	[`crate:6.0`](#crate60)
-	[`crate:6.0.5`](#crate605)
-	[`crate:6.1`](#crate61)
-	[`crate:6.1.2`](#crate612)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:5d7cd92eb84d56d538e2222a436e432164b853fdf186aebb17c446787f23a307
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:039f0fc6f1cdd3b275310e1a182a67092efb9d916b875f8c3fca811d30c5e050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232254407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9946365265397a39897876cdbc3d2c2a3c5c19c77a2c626a017dd22e96deb98f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:39 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:39 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:43:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:08 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:08 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:08 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:08 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:08 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Thu, 29 Jan 2026 18:44:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c6c90a8e86909827c53164e7490e1dfe1539d2449ad8ba1a4cdc744e87c50cf1`  
		Last Modified: Thu, 29 Jan 2026 18:12:55 GMT  
		Size: 67.5 MB (67497565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758a6eede0c4e18e6d305e9453fc23d62e7b94787291bcd53c38f80398498fec`  
		Last Modified: Thu, 29 Jan 2026 18:44:27 GMT  
		Size: 13.1 MB (13089649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6486f30ee1e17f7dd649551156444a5ac262bf7510d9fba8b07538a081ba3304`  
		Last Modified: Thu, 29 Jan 2026 18:44:30 GMT  
		Size: 149.7 MB (149721691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002d41765d3b0fdaca20621a889dad9fb51d79c76e3f426f5df52556d491e8ec`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83943f4fb15d7e65b9aded21be3275a04a5a2b3432dcd063b5bfa1cc595380fb`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b0a9edf5785a8eba96c0eb6df9e848200e89cdcf016232fe20c6cd3097bec2`  
		Last Modified: Thu, 29 Jan 2026 18:44:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dae79179780440a0001a93747b5f01de56f29eb1b01af665dd73fa8445e458`  
		Last Modified: Thu, 29 Jan 2026 18:44:28 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41efa7a19e30ef512cc695489d353c0667024551048a716815f0ff0374c66f4`  
		Last Modified: Thu, 29 Jan 2026 18:44:28 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:c359cf67bbfa4c03302067f2ac4db0973258d951719d716066998fcb7717cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5169977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23162b1290abc47dc35786eb32238b92dd7b0d4e07e1870547e6f5c07ae7fec7`

```dockerfile
```

-	Layers:
	-	`sha256:f9839916fa0c248bd355178df7f65e6d9d0f7ec1d7da3b117723c7320ef3fb25`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 5.1 MB (5147099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cae367eafec9ba203842f223716a751c9a12cf604b54e4c087a65e42efaf79`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 22.9 KB (22878 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:97713429eb89bedbaaa33dfc3c92428beb7f3e28fe1c95cc1e8c14602497bf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231465362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9accab111c788850c6c4bbb7d5bb40ae9f1553c994cfef2b4067351a2785ec93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:40 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:40 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:44:36 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:50 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:50 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:50 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:50 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Thu, 29 Jan 2026 18:44:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:dc4cc267c74fe1849185ec1aa3a49c7281f8bd96219b60eef2f570ccc68739e3`  
		Last Modified: Thu, 29 Jan 2026 18:12:58 GMT  
		Size: 66.0 MB (65978521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cd7b0ca28f8ad4d331d3304a754a9386e54db464f5e151291af2ee877294a0`  
		Last Modified: Thu, 29 Jan 2026 18:45:09 GMT  
		Size: 13.1 MB (13139010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01b901997c7618636f39b0f697d24407eaa950740b7e66dd241e0a3bff03f11`  
		Last Modified: Thu, 29 Jan 2026 18:45:12 GMT  
		Size: 150.4 MB (150402327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376e45ae9e2482deccb7e6f1d1de8d24ea1bac391d4bee33251adecbe83b6b02`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb71f39903d02b038209aa8fc7c8a37bca863e8267b3992fd869f0d04be5e1b`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35e9c651fb84365b6b098be2bc4c3a0cc982f61bf3f2c2507563f43f9c519f5`  
		Last Modified: Thu, 29 Jan 2026 18:45:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37028e40bb80ce103355f34b962c8fe4372b34e5b6727f296f0a2e14cfcdb089`  
		Last Modified: Thu, 29 Jan 2026 18:45:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa787cb3644ab1403aa2aef47544d2159607aeeeff01d96286b9ddde5488ff9`  
		Last Modified: Thu, 29 Jan 2026 18:45:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:7ac90e11873603c5a9a4f07032745afe9a3f1b11f2f3a6ed0bafc62807fa4219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d466fa286261d7a3274ad3c6fd4b1f735fc650429660db9bbae9b3082d95f29`

```dockerfile
```

-	Layers:
	-	`sha256:b63abeca543017d7fb7076e1bc25f36545140fbd2953fa5fbcfb418f0043a01d`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 5.1 MB (5144395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f866c775b74c27d68be24ac2b17ce94f3e831202229ebcce10a514bf8a0594d`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.16`

```console
$ docker pull crate@sha256:5d7cd92eb84d56d538e2222a436e432164b853fdf186aebb17c446787f23a307
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10.16` - linux; amd64

```console
$ docker pull crate@sha256:039f0fc6f1cdd3b275310e1a182a67092efb9d916b875f8c3fca811d30c5e050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232254407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9946365265397a39897876cdbc3d2c2a3c5c19c77a2c626a017dd22e96deb98f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:39 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:39 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:43:54 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:07 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:08 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:08 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:08 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:08 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:08 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Thu, 29 Jan 2026 18:44:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:08 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c6c90a8e86909827c53164e7490e1dfe1539d2449ad8ba1a4cdc744e87c50cf1`  
		Last Modified: Thu, 29 Jan 2026 18:12:55 GMT  
		Size: 67.5 MB (67497565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758a6eede0c4e18e6d305e9453fc23d62e7b94787291bcd53c38f80398498fec`  
		Last Modified: Thu, 29 Jan 2026 18:44:27 GMT  
		Size: 13.1 MB (13089649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6486f30ee1e17f7dd649551156444a5ac262bf7510d9fba8b07538a081ba3304`  
		Last Modified: Thu, 29 Jan 2026 18:44:30 GMT  
		Size: 149.7 MB (149721691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002d41765d3b0fdaca20621a889dad9fb51d79c76e3f426f5df52556d491e8ec`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83943f4fb15d7e65b9aded21be3275a04a5a2b3432dcd063b5bfa1cc595380fb`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b0a9edf5785a8eba96c0eb6df9e848200e89cdcf016232fe20c6cd3097bec2`  
		Last Modified: Thu, 29 Jan 2026 18:44:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dae79179780440a0001a93747b5f01de56f29eb1b01af665dd73fa8445e458`  
		Last Modified: Thu, 29 Jan 2026 18:44:28 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41efa7a19e30ef512cc695489d353c0667024551048a716815f0ff0374c66f4`  
		Last Modified: Thu, 29 Jan 2026 18:44:28 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.16` - unknown; unknown

```console
$ docker pull crate@sha256:c359cf67bbfa4c03302067f2ac4db0973258d951719d716066998fcb7717cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5169977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23162b1290abc47dc35786eb32238b92dd7b0d4e07e1870547e6f5c07ae7fec7`

```dockerfile
```

-	Layers:
	-	`sha256:f9839916fa0c248bd355178df7f65e6d9d0f7ec1d7da3b117723c7320ef3fb25`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 5.1 MB (5147099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cae367eafec9ba203842f223716a751c9a12cf604b54e4c087a65e42efaf79`  
		Last Modified: Thu, 29 Jan 2026 18:44:26 GMT  
		Size: 22.9 KB (22878 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10.16` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:97713429eb89bedbaaa33dfc3c92428beb7f3e28fe1c95cc1e8c14602497bf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231465362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9accab111c788850c6c4bbb7d5bb40ae9f1553c994cfef2b4067351a2785ec93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:40 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:40 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:44:36 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.16.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.16.tar.gz.asc crate-5.10.16.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.16.tar.gz.asc     && tar -xf crate-5.10.16.tar.gz -C /crate --strip-components=1     && rm crate-5.10.16.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:50 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:50 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:50 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:50 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:50 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:51 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:51 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-10T13:54:12.012567 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.16
# Thu, 29 Jan 2026 18:44:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:51 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:dc4cc267c74fe1849185ec1aa3a49c7281f8bd96219b60eef2f570ccc68739e3`  
		Last Modified: Thu, 29 Jan 2026 18:12:58 GMT  
		Size: 66.0 MB (65978521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cd7b0ca28f8ad4d331d3304a754a9386e54db464f5e151291af2ee877294a0`  
		Last Modified: Thu, 29 Jan 2026 18:45:09 GMT  
		Size: 13.1 MB (13139010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01b901997c7618636f39b0f697d24407eaa950740b7e66dd241e0a3bff03f11`  
		Last Modified: Thu, 29 Jan 2026 18:45:12 GMT  
		Size: 150.4 MB (150402327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376e45ae9e2482deccb7e6f1d1de8d24ea1bac391d4bee33251adecbe83b6b02`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb71f39903d02b038209aa8fc7c8a37bca863e8267b3992fd869f0d04be5e1b`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35e9c651fb84365b6b098be2bc4c3a0cc982f61bf3f2c2507563f43f9c519f5`  
		Last Modified: Thu, 29 Jan 2026 18:45:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37028e40bb80ce103355f34b962c8fe4372b34e5b6727f296f0a2e14cfcdb089`  
		Last Modified: Thu, 29 Jan 2026 18:45:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa787cb3644ab1403aa2aef47544d2159607aeeeff01d96286b9ddde5488ff9`  
		Last Modified: Thu, 29 Jan 2026 18:45:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10.16` - unknown; unknown

```console
$ docker pull crate@sha256:7ac90e11873603c5a9a4f07032745afe9a3f1b11f2f3a6ed0bafc62807fa4219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d466fa286261d7a3274ad3c6fd4b1f735fc650429660db9bbae9b3082d95f29`

```dockerfile
```

-	Layers:
	-	`sha256:b63abeca543017d7fb7076e1bc25f36545140fbd2953fa5fbcfb418f0043a01d`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 5.1 MB (5144395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f866c775b74c27d68be24ac2b17ce94f3e831202229ebcce10a514bf8a0594d`  
		Last Modified: Thu, 29 Jan 2026 18:45:08 GMT  
		Size: 23.0 KB (23003 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0`

```console
$ docker pull crate@sha256:d43d395b2a7322b6b7d735f7c1bebefd92dc11b9429cce7f156a71c92fc95737
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0` - linux; amd64

```console
$ docker pull crate@sha256:9b9d84bcf618889976aa42a709805bbb6bbbf1382f53fa6816671d371c102c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231561480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2190c912676fcd44095b46a1c90a5afa200b4a61431db20fad95487c53fec784`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:39 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:39 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:43:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:03 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:03 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:03 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:03 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Thu, 29 Jan 2026 18:44:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c6c90a8e86909827c53164e7490e1dfe1539d2449ad8ba1a4cdc744e87c50cf1`  
		Last Modified: Thu, 29 Jan 2026 18:12:55 GMT  
		Size: 67.5 MB (67497565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeedb32dc18bd6b4858fc7505b5654d6b516d77d3a61a25f89bb0c54a2c283c`  
		Last Modified: Thu, 29 Jan 2026 18:44:22 GMT  
		Size: 13.1 MB (13089627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42337d92985e8a6709eda6b9c562d8693f3d9b73a14a62911048b1a685411c0`  
		Last Modified: Thu, 29 Jan 2026 18:44:25 GMT  
		Size: 149.0 MB (149028784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da486bc0c29737f2fe7807e60645a8b70048f4125047431af0329ba5002983`  
		Last Modified: Thu, 29 Jan 2026 18:44:22 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd73dc66b5300dd389ac9636f0e6ef8236b489872bd7886716748820c8aa0fa`  
		Last Modified: Thu, 29 Jan 2026 18:44:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe325fe47f84bfea1a8b0dc1c1c355915c1cbb0136512d7c7965b7a76cacb44`  
		Last Modified: Thu, 29 Jan 2026 18:44:23 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb3519450bd0af3820ac439c04e01769b600abdd2cd7645af4b34b8cf6cc60`  
		Last Modified: Thu, 29 Jan 2026 18:44:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e2b907dc160c1acd525162c930544e747cf93babf574546adb23dee295443`  
		Last Modified: Thu, 29 Jan 2026 18:44:23 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:dc741d4b2a1abf0a1fb3de37a54e272507ef8addc8945cf571ac0563b8dbe2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652229e37df02cfb365523e8cfe3160137908f9d2b89c7ed1a5f41d08f97fa76`

```dockerfile
```

-	Layers:
	-	`sha256:9f8542aa992e19a18f4d66c07e1cc0d74f153b48d142f98a904bd2921f2968a2`  
		Last Modified: Thu, 29 Jan 2026 18:44:21 GMT  
		Size: 5.2 MB (5150237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff364a5c36bf571cc0bd6434275bf976dfc51aedbb8a90893331821a39ec7c91`  
		Last Modified: Thu, 29 Jan 2026 18:44:21 GMT  
		Size: 22.8 KB (22842 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:526c070e370fa64587632b19b1fbc4d4ae0b1071ba83089df868bf2c8062c9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230779258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15001e23c1d89bbd646aed3d79a93c48a6685f0e9d0e11a73a1b44a968430145`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:40 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:40 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:44:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:41 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:41 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:41 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:41 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Thu, 29 Jan 2026 18:44:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:dc4cc267c74fe1849185ec1aa3a49c7281f8bd96219b60eef2f570ccc68739e3`  
		Last Modified: Thu, 29 Jan 2026 18:12:58 GMT  
		Size: 66.0 MB (65978521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90cb1f5ae2971f33638e71c9e7591442bf33afba49dfd17951f6d859ddb5192`  
		Last Modified: Thu, 29 Jan 2026 18:45:00 GMT  
		Size: 13.1 MB (13139045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbb2430ae14165930beed86f56a15f7fe46c203d098a377f9d7f390e139622c`  
		Last Modified: Thu, 29 Jan 2026 18:45:03 GMT  
		Size: 149.7 MB (149716187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ec825686d7177dd0387c6606e535bde167a2d78a1b5af4383e6f201b785bc`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31480021faf7d85549a531e3f9f79ab2540b2357b92408c7354579b77d374b0`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6981ad112ae0fc597489f369e5b1069a4e1d1be03f93c02188c39b1a9b1d73c`  
		Last Modified: Thu, 29 Jan 2026 18:45:00 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88975fb6af29c4c4dfa3cc9d251a8600792916197e15cb246e7e4aa1e4d00895`  
		Last Modified: Thu, 29 Jan 2026 18:45:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383117dc180b7e20c978a44586f37dbc0cf0f4420dee75b0a198777c87e6364`  
		Last Modified: Thu, 29 Jan 2026 18:45:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0` - unknown; unknown

```console
$ docker pull crate@sha256:6ffd17356d194bb3b36e67add584c4e7186304a152ece29388389c74db22787c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ecd9e1bd369cf0991928246e6baea558e40a1fa313aeed2886003e24a78ed`

```dockerfile
```

-	Layers:
	-	`sha256:c78580ce3cfdf75ce707fa92a3717854d37d4deb68ab0bc33dad123365076d07`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 5.1 MB (5148144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf93f8751719e1af523dbde460e9ceda63e830715459692eb871273fbb7d120`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.0.5`

```console
$ docker pull crate@sha256:d43d395b2a7322b6b7d735f7c1bebefd92dc11b9429cce7f156a71c92fc95737
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.0.5` - linux; amd64

```console
$ docker pull crate@sha256:9b9d84bcf618889976aa42a709805bbb6bbbf1382f53fa6816671d371c102c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231561480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2190c912676fcd44095b46a1c90a5afa200b4a61431db20fad95487c53fec784`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:39 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:39 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:43:49 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:03 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:03 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:03 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:03 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:03 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Thu, 29 Jan 2026 18:44:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:03 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:c6c90a8e86909827c53164e7490e1dfe1539d2449ad8ba1a4cdc744e87c50cf1`  
		Last Modified: Thu, 29 Jan 2026 18:12:55 GMT  
		Size: 67.5 MB (67497565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeedb32dc18bd6b4858fc7505b5654d6b516d77d3a61a25f89bb0c54a2c283c`  
		Last Modified: Thu, 29 Jan 2026 18:44:22 GMT  
		Size: 13.1 MB (13089627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42337d92985e8a6709eda6b9c562d8693f3d9b73a14a62911048b1a685411c0`  
		Last Modified: Thu, 29 Jan 2026 18:44:25 GMT  
		Size: 149.0 MB (149028784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da486bc0c29737f2fe7807e60645a8b70048f4125047431af0329ba5002983`  
		Last Modified: Thu, 29 Jan 2026 18:44:22 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd73dc66b5300dd389ac9636f0e6ef8236b489872bd7886716748820c8aa0fa`  
		Last Modified: Thu, 29 Jan 2026 18:44:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe325fe47f84bfea1a8b0dc1c1c355915c1cbb0136512d7c7965b7a76cacb44`  
		Last Modified: Thu, 29 Jan 2026 18:44:23 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb3519450bd0af3820ac439c04e01769b600abdd2cd7645af4b34b8cf6cc60`  
		Last Modified: Thu, 29 Jan 2026 18:44:23 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e2b907dc160c1acd525162c930544e747cf93babf574546adb23dee295443`  
		Last Modified: Thu, 29 Jan 2026 18:44:23 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.5` - unknown; unknown

```console
$ docker pull crate@sha256:dc741d4b2a1abf0a1fb3de37a54e272507ef8addc8945cf571ac0563b8dbe2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652229e37df02cfb365523e8cfe3160137908f9d2b89c7ed1a5f41d08f97fa76`

```dockerfile
```

-	Layers:
	-	`sha256:9f8542aa992e19a18f4d66c07e1cc0d74f153b48d142f98a904bd2921f2968a2`  
		Last Modified: Thu, 29 Jan 2026 18:44:21 GMT  
		Size: 5.2 MB (5150237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff364a5c36bf571cc0bd6434275bf976dfc51aedbb8a90893331821a39ec7c91`  
		Last Modified: Thu, 29 Jan 2026 18:44:21 GMT  
		Size: 22.8 KB (22842 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:6.0.5` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:526c070e370fa64587632b19b1fbc4d4ae0b1071ba83089df868bf2c8062c9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230779258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15001e23c1d89bbd646aed3d79a93c48a6685f0e9d0e11a73a1b44a968430145`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 29 Jan 2026 18:12:40 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Thu, 29 Jan 2026 18:12:40 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 18:44:27 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Thu, 29 Jan 2026 18:44:40 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-6.0.5.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-6.0.5.tar.gz.asc crate-6.0.5.tar.gz     && rm -rf "$GNUPGHOME" crate-6.0.5.tar.gz.asc     && tar -xf crate-6.0.5.tar.gz -C /crate --strip-components=1     && rm crate-6.0.5.tar.gz # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 18:44:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 29 Jan 2026 18:44:41 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:44:41 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:44:41 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Thu, 29 Jan 2026 18:44:41 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Thu, 29 Jan 2026 18:44:41 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-12-11T15:38:12.972308 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=6.0.5
# Thu, 29 Jan 2026 18:44:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 29 Jan 2026 18:44:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:44:42 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:dc4cc267c74fe1849185ec1aa3a49c7281f8bd96219b60eef2f570ccc68739e3`  
		Last Modified: Thu, 29 Jan 2026 18:12:58 GMT  
		Size: 66.0 MB (65978521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90cb1f5ae2971f33638e71c9e7591442bf33afba49dfd17951f6d859ddb5192`  
		Last Modified: Thu, 29 Jan 2026 18:45:00 GMT  
		Size: 13.1 MB (13139045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbb2430ae14165930beed86f56a15f7fe46c203d098a377f9d7f390e139622c`  
		Last Modified: Thu, 29 Jan 2026 18:45:03 GMT  
		Size: 149.7 MB (149716187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ec825686d7177dd0387c6606e535bde167a2d78a1b5af4383e6f201b785bc`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 1.9 MB (1943623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31480021faf7d85549a531e3f9f79ab2540b2357b92408c7354579b77d374b0`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6981ad112ae0fc597489f369e5b1069a4e1d1be03f93c02188c39b1a9b1d73c`  
		Last Modified: Thu, 29 Jan 2026 18:45:00 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88975fb6af29c4c4dfa3cc9d251a8600792916197e15cb246e7e4aa1e4d00895`  
		Last Modified: Thu, 29 Jan 2026 18:45:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383117dc180b7e20c978a44586f37dbc0cf0f4420dee75b0a198777c87e6364`  
		Last Modified: Thu, 29 Jan 2026 18:45:01 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:6.0.5` - unknown; unknown

```console
$ docker pull crate@sha256:6ffd17356d194bb3b36e67add584c4e7186304a152ece29388389c74db22787c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ecd9e1bd369cf0991928246e6baea558e40a1fa313aeed2886003e24a78ed`

```dockerfile
```

-	Layers:
	-	`sha256:c78580ce3cfdf75ce707fa92a3717854d37d4deb68ab0bc33dad123365076d07`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 5.1 MB (5148144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf93f8751719e1af523dbde460e9ceda63e830715459692eb871273fbb7d120`  
		Last Modified: Thu, 29 Jan 2026 18:44:59 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:6.1`

```console
$ docker pull crate@sha256:b29cb49440c3780e97862409337ce312e9f7a33eeee2ad5b539f229dbb091755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1` - linux; amd64

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

### `crate:6.1` - unknown; unknown

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

### `crate:6.1` - linux; arm64 variant v8

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

### `crate:6.1` - unknown; unknown

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

## `crate:6.1.2`

```console
$ docker pull crate@sha256:b29cb49440c3780e97862409337ce312e9f7a33eeee2ad5b539f229dbb091755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:6.1.2` - linux; amd64

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

### `crate:6.1.2` - unknown; unknown

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

### `crate:6.1.2` - linux; arm64 variant v8

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

### `crate:6.1.2` - unknown; unknown

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
