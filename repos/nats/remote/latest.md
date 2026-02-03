## `nats:latest`

```console
$ docker pull nats@sha256:459cecd28a535a35f88606da507efd9de763cd4f0cf5bc92fce968f7ff80aef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4648; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:a5e4660894cd794c2ce9069e3e43761e8d32c9c06ea527c053604b96d48647c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6598587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1f5e399cbaed2d4545b4e27fdb74af75cd18c9ca268c6d36043db0747ac67`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 03:59:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Jan 2026 03:59:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 28 Jan 2026 03:59:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 28 Jan 2026 03:59:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 03:59:18 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Jan 2026 03:59:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f8912005071f27ea416bffea2294316df3b1b12b1e8346b2a1adcd792aa8496`  
		Last Modified: Tue, 27 Jan 2026 16:11:14 GMT  
		Size: 6.6 MB (6598078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5b11b6a135c91aa1d5b765ea56500eb4444b7cf01bd35c19e7ac2ab9e1119f`  
		Last Modified: Wed, 28 Jan 2026 03:59:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:fdb00d831d5690a779b93fb10fd4a10b0a1f5b33a1ffce47c16c0ea83c5ce8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edcc4922c3b5e316c90758dea2008995ff11e0c6f37c3f0149e62704d6a486d`

```dockerfile
```

-	Layers:
	-	`sha256:881ee6abf87bdec49ef80923dfc7dd695c9fc6946a03f9c32214b15ae0cd91aa`  
		Last Modified: Wed, 28 Jan 2026 03:59:22 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:a598851514cb7b1b66b3c657ce6c8a42e1a00b6bcbdf57b2d81cbff6b838007a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6323104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ad3d8abc2ef3503c041589a59814dd5ef97b9acc86df9a50b6515a7802e5bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Jan 2026 03:49:43 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 03:49:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1efb0795d882364e2a023f0af5959b157fb2940eacdb92639318b205267c0ad4`  
		Last Modified: Tue, 27 Jan 2026 16:11:11 GMT  
		Size: 6.3 MB (6322595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41adab603476e09c828796f646ae1e7715c416878b36c9bb6e078049de485f60`  
		Last Modified: Wed, 28 Jan 2026 03:49:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6c0e0658b56fba5e24e4cc7a736a0bfe0bfe7e0a177c2cf599564943cfb2d856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc6b2d1f15edc82c952153597736ef2d116b614993b114ea4fefd10b1e4cc16`

```dockerfile
```

-	Layers:
	-	`sha256:9bda1cdc61ac3ccd294b760e0eb7618f50cc293b71c7b6b4b11ae048f33aca6b`  
		Last Modified: Wed, 28 Jan 2026 03:49:47 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:64109e8280e8120cb104f0471dd29f531933b9c37b7c1334fe494cde3a5c50cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6310861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b70c2c58d6f75ebd013e1415ecdc44e84cbd00e62dd066a4107d7029e6d32d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 03:51:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Jan 2026 03:51:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 28 Jan 2026 03:51:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 28 Jan 2026 03:51:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 03:51:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Jan 2026 03:51:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f89bd8d5669bd18e009b01f3649659381ff93c4199e64ffa25637a2739cba3a5`  
		Last Modified: Tue, 27 Jan 2026 16:11:12 GMT  
		Size: 6.3 MB (6310353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ba46762fabeeb80a08d47d42e77e37f2068352863068b2be6fd6956444c2bb`  
		Last Modified: Wed, 28 Jan 2026 03:52:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:301d82cbd806e8cc14fe6b4b885b84111f2ab624239bd8f915092dcf274410ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849037396fb4072f90f6d160d76dd5df092f2311dd6daa9dc7a95f91f4f85d8f`

```dockerfile
```

-	Layers:
	-	`sha256:d3c98735cfaf8922f3d87a37f30b610f844cc47adb033708562d33f6d2862d41`  
		Last Modified: Wed, 28 Jan 2026 03:52:01 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d36bca4ff2cbbe62b210a7de99266abef1146fddffd51b99f8074ac2e1f0c58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42786aa06e320fdbad53f504ade6254a85664195ff2ac74d4c3c9f3dd08b537`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 04:20:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Jan 2026 04:20:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 28 Jan 2026 04:20:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 28 Jan 2026 04:20:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 04:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Jan 2026 04:20:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e69d87f2a1b2cfbc091bf2d3af13a1d9188b163cbfbce527d6fb245cd470e987`  
		Last Modified: Tue, 27 Jan 2026 16:11:12 GMT  
		Size: 6.0 MB (6009325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce9530142284cad954b7afcdb0325f685eb8a4c4d5ae36caebb0bfbe92f5bba`  
		Last Modified: Wed, 28 Jan 2026 04:20:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:68d83761f0e6e6486757150c1d3ee54e793e8d38ab449fd6c472b5dd9600682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cabadf46fa50dcddfa3426cd0c3e78184ec490e744c4d7075dfc94e3c199929`

```dockerfile
```

-	Layers:
	-	`sha256:0453214c68bd5c178dfaf3315e10158c45e21c0b7659f081f60ab76b280f7578`  
		Last Modified: Wed, 28 Jan 2026 04:20:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:805ecb7060072c01ff3dc91e05207213c9ff8de96ac7bb68b0a848ea1270eaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6059946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c293c9cca9fa9c0f9530879af4a40f35b8985690e2f3044ee95e153228dcab8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 05:51:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Jan 2026 05:51:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 28 Jan 2026 05:51:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 28 Jan 2026 05:51:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 05:51:55 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Jan 2026 05:51:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7498e46ed99a6f25a5e161fffb2a10e547d3bd8f682806db51e70bf75c104d8`  
		Last Modified: Tue, 27 Jan 2026 16:11:14 GMT  
		Size: 6.1 MB (6059437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eba08ec63c6a6cfb9399d5cb44979b8c213b0bff1888cb535469c0cb49b2d4`  
		Last Modified: Wed, 28 Jan 2026 05:52:02 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:45c844196711301dc573cc3af551105265133de3d721b4f4686778da8a5df81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611de58748d3ff363b35154db81713e94d394be7da439f3f8a37c93607d3bfef`

```dockerfile
```

-	Layers:
	-	`sha256:ef432194a4eb78b35b2541790ce4690fe016896a3e127d7ef421d1afdbb8108c`  
		Last Modified: Wed, 28 Jan 2026 05:52:02 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:465326ca4b2d0747ea17d557be583302e212b64470f000f5fc5fc1e9ea74e23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af706c38b36e762c008b80b9801089474425437ae56c0850bbc86eb3b65a872`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 07:00:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 28 Jan 2026 07:00:45 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 28 Jan 2026 07:00:45 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 28 Jan 2026 07:00:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 07:00:45 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 28 Jan 2026 07:00:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:647f636b2ba788fbcd64742e49cd42dbe55579be711374f52ac5c9e3bb6810d2`  
		Last Modified: Tue, 27 Jan 2026 16:11:14 GMT  
		Size: 6.4 MB (6439063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be840e3eabe1376e97e66367790c31cae37541af667f924f8d151b378b89472`  
		Last Modified: Wed, 28 Jan 2026 07:00:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:feac11d1a516c84cbe09bdf9047c67e337f3963467be1448c6e7b2f261436bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46dc0c8a4cae0e16fce1f57e0304f3c2b1301f0db8c35d8e19bb65002042105`

```dockerfile
```

-	Layers:
	-	`sha256:e60d319a9bc6178679573aff629faca51ef4202bb30280f65caca92303621985`  
		Last Modified: Wed, 28 Jan 2026 07:00:52 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.4648; amd64

```console
$ docker pull nats@sha256:6a03415ac210d093eeae436ac6f854f14b05b33cfa275ed4cceda3ce15bd21f0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133477809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6a1273e9d934f34664ea07d20ee6e4ae25774a5f98d3c9d3c969f0f2f79cc2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 27 Jan 2026 21:20:00 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 27 Jan 2026 21:20:01 GMT
RUN cmd /S /C #(nop) COPY file:20b20f3f8110d9ab945899af7971e9305a5d983e52683439f0ed26eaec266894 in C:\nats-server.exe 
# Tue, 27 Jan 2026 21:20:02 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 27 Jan 2026 21:20:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 27 Jan 2026 21:20:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 27 Jan 2026 21:20:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187a3d092a340c8ac86013d048353e3fc9c84f9bd56954e139d32eacf2dd0cb3`  
		Last Modified: Tue, 27 Jan 2026 21:20:09 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e7e72a48cce95619bbd2c5781f092d55e8bc19a68431f8b6eaa223ff1bef4`  
		Last Modified: Tue, 27 Jan 2026 21:20:09 GMT  
		Size: 6.8 MB (6775036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102b440fc8d7ffea4f1db79f552bf440543016cd8f5933360374f8ac5aa2a620`  
		Last Modified: Tue, 27 Jan 2026 21:20:07 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f05a393bd45550e9f9e6a2c97cd185272846c851af0a08a165f66886650ae1e`  
		Last Modified: Tue, 27 Jan 2026 21:20:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f780bc2f41363d3b55e2b296b2aa32fba1a54b450f95b6f1f65d3739319017`  
		Last Modified: Tue, 27 Jan 2026 21:20:08 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a26979d92944e7837e92b7df85121485afae22367322d3563eadb043207cd`  
		Last Modified: Tue, 27 Jan 2026 21:20:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
