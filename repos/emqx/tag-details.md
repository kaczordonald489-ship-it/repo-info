<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.8`](#emqx588)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:7523daa7d67219a554cf58722140a7a0e1cb4981d19c2d571652252eb1832291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:e3ce192cbc56630ad6d4b73cc84ed58584c859e243d8106c975d8f9c630cc8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79555f1893a01da11fc382a74957ce775332fd258d625f60e207597c9c61cb6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:03:10 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 04:03:10 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 04:03:10 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 04:03:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 04:03:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 04:03:10 GMT
USER emqx
# Tue, 18 Nov 2025 04:03:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 04:03:10 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 04:03:10 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46039848836884c828d3e66049078c42f342e084cdf3b914a34fef270bf66618`  
		Last Modified: Tue, 18 Nov 2025 04:03:39 GMT  
		Size: 78.6 MB (78621688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c18b882624e2c96a3f358cc763dfd9303d3376fb79d7350e4f568f201e6a9b`  
		Last Modified: Tue, 18 Nov 2025 04:03:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:cc9795b81aaacffa01210d5131c4575441fec4b3532276b3cfedc09650d1238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642fb15bf0cd09d2fc4e3166d26c9706e106ebb58e756c55e21b53a6c36f1eb2`

```dockerfile
```

-	Layers:
	-	`sha256:fd2472473fedc9f7783d517d0364783a7d884a2ab702440be5266806aa7ec256`  
		Last Modified: Tue, 18 Nov 2025 06:28:12 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec5afd046ae2b7c150e3c71d3d2b5f944c5826e5a2a1bb6cb1e280fd90ca59d`  
		Last Modified: Tue, 18 Nov 2025 06:28:13 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:390d7eff32ad0b9af650a984540b3f42a598506d1b72cfbe8bce857e88e7b42f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:706939c199741d1a1e96e8ea7eeeb84fbb1ee57672a364c7e0f658c7400d95c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21aba2d89d08751153580049c82d491f5254f2b946c8384971697bd8b319c19`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:02:44 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 18 Nov 2025 04:02:44 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 18 Nov 2025 04:02:44 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 18 Nov 2025 04:02:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 04:02:44 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 04:02:44 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 04:02:44 GMT
USER emqx
# Tue, 18 Nov 2025 04:02:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 04:02:44 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 04:02:44 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 04:02:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:02:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1299a0d78b2f9d796c25388b1e5812d9e956f8d9dcc5fb0a725e2058d9bf`  
		Last Modified: Tue, 18 Nov 2025 04:03:16 GMT  
		Size: 97.2 MB (97155116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659ab90fe021759e75d1fc094040a60f70cd017fdc773c0c1d6bdfca8b47a57`  
		Last Modified: Tue, 18 Nov 2025 04:03:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:2c3740be82d1c5264b82f424ae40e69f7ac9b761b89fc3a2d15305cf28e8c71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a6e3ba0168bee4d10b6585a7c83fff9f7c75cd7da30e9eaafa62446654ef6e`

```dockerfile
```

-	Layers:
	-	`sha256:f2c1117d807310f236c74f4843c5a7068cd06c757b94af28a6b1da07039ead2a`  
		Last Modified: Tue, 18 Nov 2025 06:28:17 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dab4c255bab5930e68bd4e4148dff85895367ad587f3950cfd8a79677ebdee0`  
		Last Modified: Tue, 18 Nov 2025 06:28:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8dd176f815a25b03e1e890aa0f8d69440a2b2dc3c3b8b1e20ceca36492a2699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1059914f9f4a03cb7d34ff2b8b63b4e32ac71537cb8a7e5512e31fa35c6fa1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:11 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 18 Nov 2025 02:14:11 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 18 Nov 2025 02:14:11 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 18 Nov 2025 02:14:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:14:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:14:11 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:14:11 GMT
USER emqx
# Tue, 18 Nov 2025 02:14:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:14:11 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:14:12 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:14:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:14:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d526c0043df2310fc7956a7d5b8fee30f7b1baa9ed990bd2eb9ed4079f7db674`  
		Last Modified: Tue, 18 Nov 2025 02:14:59 GMT  
		Size: 93.7 MB (93715171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514a376a62d1f5c69acc4ca0a77576694629ba819d8f43651e13082aff9a2220`  
		Last Modified: Tue, 18 Nov 2025 02:14:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:3b1705652cd4eb5650e74614edaa5d5ff915433ac5c7c6a009862448ebe5b1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172e0218f632dbd46ebd950dfe4380b601012fc68cbd45d26e47c4066908a501`

```dockerfile
```

-	Layers:
	-	`sha256:b6fc605599f1d5602815447fae8b4dbb80e49a9bf516fd63adcb44bf74f532b2`  
		Last Modified: Tue, 18 Nov 2025 03:30:41 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae369c3d4bd51fa2545bec90a1106320df4829ec88330c726aae0f779781f93`  
		Last Modified: Tue, 18 Nov 2025 03:30:42 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:390d7eff32ad0b9af650a984540b3f42a598506d1b72cfbe8bce857e88e7b42f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:706939c199741d1a1e96e8ea7eeeb84fbb1ee57672a364c7e0f658c7400d95c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21aba2d89d08751153580049c82d491f5254f2b946c8384971697bd8b319c19`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:02:44 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 18 Nov 2025 04:02:44 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 18 Nov 2025 04:02:44 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 18 Nov 2025 04:02:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 04:02:44 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 04:02:44 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 04:02:44 GMT
USER emqx
# Tue, 18 Nov 2025 04:02:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 04:02:44 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 04:02:44 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 04:02:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:02:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1299a0d78b2f9d796c25388b1e5812d9e956f8d9dcc5fb0a725e2058d9bf`  
		Last Modified: Tue, 18 Nov 2025 04:03:16 GMT  
		Size: 97.2 MB (97155116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659ab90fe021759e75d1fc094040a60f70cd017fdc773c0c1d6bdfca8b47a57`  
		Last Modified: Tue, 18 Nov 2025 04:03:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:2c3740be82d1c5264b82f424ae40e69f7ac9b761b89fc3a2d15305cf28e8c71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a6e3ba0168bee4d10b6585a7c83fff9f7c75cd7da30e9eaafa62446654ef6e`

```dockerfile
```

-	Layers:
	-	`sha256:f2c1117d807310f236c74f4843c5a7068cd06c757b94af28a6b1da07039ead2a`  
		Last Modified: Tue, 18 Nov 2025 06:28:17 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dab4c255bab5930e68bd4e4148dff85895367ad587f3950cfd8a79677ebdee0`  
		Last Modified: Tue, 18 Nov 2025 06:28:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8dd176f815a25b03e1e890aa0f8d69440a2b2dc3c3b8b1e20ceca36492a2699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1059914f9f4a03cb7d34ff2b8b63b4e32ac71537cb8a7e5512e31fa35c6fa1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:11 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 18 Nov 2025 02:14:11 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 18 Nov 2025 02:14:11 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 18 Nov 2025 02:14:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:14:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:14:11 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:14:11 GMT
USER emqx
# Tue, 18 Nov 2025 02:14:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:14:11 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:14:12 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:14:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:14:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d526c0043df2310fc7956a7d5b8fee30f7b1baa9ed990bd2eb9ed4079f7db674`  
		Last Modified: Tue, 18 Nov 2025 02:14:59 GMT  
		Size: 93.7 MB (93715171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514a376a62d1f5c69acc4ca0a77576694629ba819d8f43651e13082aff9a2220`  
		Last Modified: Tue, 18 Nov 2025 02:14:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:3b1705652cd4eb5650e74614edaa5d5ff915433ac5c7c6a009862448ebe5b1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172e0218f632dbd46ebd950dfe4380b601012fc68cbd45d26e47c4066908a501`

```dockerfile
```

-	Layers:
	-	`sha256:b6fc605599f1d5602815447fae8b4dbb80e49a9bf516fd63adcb44bf74f532b2`  
		Last Modified: Tue, 18 Nov 2025 03:30:41 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae369c3d4bd51fa2545bec90a1106320df4829ec88330c726aae0f779781f93`  
		Last Modified: Tue, 18 Nov 2025 03:30:42 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:7523daa7d67219a554cf58722140a7a0e1cb4981d19c2d571652252eb1832291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:e3ce192cbc56630ad6d4b73cc84ed58584c859e243d8106c975d8f9c630cc8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79555f1893a01da11fc382a74957ce775332fd258d625f60e207597c9c61cb6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:03:10 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 04:03:10 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 04:03:10 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 04:03:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 04:03:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 04:03:10 GMT
USER emqx
# Tue, 18 Nov 2025 04:03:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 04:03:10 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 04:03:10 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46039848836884c828d3e66049078c42f342e084cdf3b914a34fef270bf66618`  
		Last Modified: Tue, 18 Nov 2025 04:03:39 GMT  
		Size: 78.6 MB (78621688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c18b882624e2c96a3f358cc763dfd9303d3376fb79d7350e4f568f201e6a9b`  
		Last Modified: Tue, 18 Nov 2025 04:03:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:cc9795b81aaacffa01210d5131c4575441fec4b3532276b3cfedc09650d1238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642fb15bf0cd09d2fc4e3166d26c9706e106ebb58e756c55e21b53a6c36f1eb2`

```dockerfile
```

-	Layers:
	-	`sha256:fd2472473fedc9f7783d517d0364783a7d884a2ab702440be5266806aa7ec256`  
		Last Modified: Tue, 18 Nov 2025 06:28:12 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec5afd046ae2b7c150e3c71d3d2b5f944c5826e5a2a1bb6cb1e280fd90ca59d`  
		Last Modified: Tue, 18 Nov 2025 06:28:13 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:7523daa7d67219a554cf58722140a7a0e1cb4981d19c2d571652252eb1832291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:e3ce192cbc56630ad6d4b73cc84ed58584c859e243d8106c975d8f9c630cc8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79555f1893a01da11fc382a74957ce775332fd258d625f60e207597c9c61cb6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:03:10 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 04:03:10 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 04:03:10 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 04:03:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 04:03:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 04:03:10 GMT
USER emqx
# Tue, 18 Nov 2025 04:03:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 04:03:10 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 04:03:10 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46039848836884c828d3e66049078c42f342e084cdf3b914a34fef270bf66618`  
		Last Modified: Tue, 18 Nov 2025 04:03:39 GMT  
		Size: 78.6 MB (78621688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c18b882624e2c96a3f358cc763dfd9303d3376fb79d7350e4f568f201e6a9b`  
		Last Modified: Tue, 18 Nov 2025 04:03:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:cc9795b81aaacffa01210d5131c4575441fec4b3532276b3cfedc09650d1238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642fb15bf0cd09d2fc4e3166d26c9706e106ebb58e756c55e21b53a6c36f1eb2`

```dockerfile
```

-	Layers:
	-	`sha256:fd2472473fedc9f7783d517d0364783a7d884a2ab702440be5266806aa7ec256`  
		Last Modified: Tue, 18 Nov 2025 06:28:12 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec5afd046ae2b7c150e3c71d3d2b5f944c5826e5a2a1bb6cb1e280fd90ca59d`  
		Last Modified: Tue, 18 Nov 2025 06:28:13 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:7523daa7d67219a554cf58722140a7a0e1cb4981d19c2d571652252eb1832291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:e3ce192cbc56630ad6d4b73cc84ed58584c859e243d8106c975d8f9c630cc8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79555f1893a01da11fc382a74957ce775332fd258d625f60e207597c9c61cb6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:03:10 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 04:03:10 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 04:03:10 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 04:03:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 04:03:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 04:03:10 GMT
USER emqx
# Tue, 18 Nov 2025 04:03:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 04:03:10 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 04:03:10 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 04:03:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46039848836884c828d3e66049078c42f342e084cdf3b914a34fef270bf66618`  
		Last Modified: Tue, 18 Nov 2025 04:03:39 GMT  
		Size: 78.6 MB (78621688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c18b882624e2c96a3f358cc763dfd9303d3376fb79d7350e4f568f201e6a9b`  
		Last Modified: Tue, 18 Nov 2025 04:03:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:cc9795b81aaacffa01210d5131c4575441fec4b3532276b3cfedc09650d1238e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642fb15bf0cd09d2fc4e3166d26c9706e106ebb58e756c55e21b53a6c36f1eb2`

```dockerfile
```

-	Layers:
	-	`sha256:fd2472473fedc9f7783d517d0364783a7d884a2ab702440be5266806aa7ec256`  
		Last Modified: Tue, 18 Nov 2025 06:28:12 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec5afd046ae2b7c150e3c71d3d2b5f944c5826e5a2a1bb6cb1e280fd90ca59d`  
		Last Modified: Tue, 18 Nov 2025 06:28:13 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json
