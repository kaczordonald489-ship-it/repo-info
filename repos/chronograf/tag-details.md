<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.9`](#chronograf1109)
-	[`chronograf:1.10.9-alpine`](#chronograf1109-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:6bde6bedb800ff25d56a2138e23b1815c4f4a01ebb61520c9121607d21479fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:45aa7da8fd07c917f0b81b9229354f097ec81dbfc40d9e25bfbef2cfc0f72228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239fbd47e9acd33f72205fa2700b29a57b528c1b7defc3ab58e3ad54fe348b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d832a8b23bd03ee26616a22b1c1e726107955d2bb687b64d1abf55d80b9ef46`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 7.9 MB (7879833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0866d8ff3c769213e4f45f07b683ca8fbe9d3884d9550524c69cf8a9e0a14d0c`  
		Last Modified: Tue, 03 Feb 2026 02:43:57 GMT  
		Size: 48.9 MB (48867868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ca67b260ec18a154423f0bb4a80104a1fa46fcd4c081f87e39ebf4d49f8cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897073ceef77ec5ec1763d1ba23bf9c117ea150ac1d246acfce144bc41eb9a41`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f884f96a9a13252fe3683d44606dc301967a92be82099a04f4284840521d5d9`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4186f1511d79fa944ef29f8288220efb49b030414016bffcdcc2a758cd529c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14086ce4dff01c2ae6810168e2dc833e98be020fb77101da309f97f5a31bea15`

```dockerfile
```

-	Layers:
	-	`sha256:96c0e54a1af2614a4429deb8fd8804388343d9294fcc6fca433f614084b582fc`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d54c1e3b5b8d8bcc4aff8c1e3090462fe76e012c2be268e35e3a55d4bb47c86`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:caacc6adbf2c4452766148b57d7999e190d5e1b879e600c8ae910a756cab9ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76790750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376ba31d0de7000782f5544cc1e6f54bfc40b5a09f2cf792ca5ceee9c0715cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:35:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 03:35:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:35:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:35:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:35:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb933aee84f3061780dc62fe2a11f8a092938c1f0128dc3e0cc478f20cae5f03`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 6.5 MB (6512172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d8f86617386920707c6dcb5bcfeaecd5519f37e0b72b40e6dc85634448615c`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 46.3 MB (46320011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b9281433f890ca914638da3dbe7a259675320d4141a66c3c2c5618d16cdae7`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94313802f27736d53e49c2875005d79d9778deef7bba174bb12e589caf4863`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eafeff883d8a20a4a4985fdc001c46d135191f83255afdf70f3ca85f39f5ee`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d86d4ff611eba3aca600330c6a93b1ea23dfcffecd2dcab1e4fa74a6c800b572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb657b8dadf271f5de60a3a5bb024eda6f7a77168ea9f6ba6a593244123bc872`

```dockerfile
```

-	Layers:
	-	`sha256:5baf10006c61e2d5e257d76091f8f47dd1ca2973e1a47dd49f5e05d014e9c794`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b4b973bf15b61969d583df457b7db1bf4d323dc98aefb6114f6128a9a36999`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7c2925db5538718fe241a5ac3c233ef2112488a77d312ea9f4a9e83da0285565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81837759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fb1b21e6b2cb9ae6d9e52fc2d7e6bd1696d589c2c3f7a02d56d89fc5abd62e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:47 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:46:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73dec86f6dcfcd53df4db205f0e03292a615a504cc3cdd11a76253b1212154`  
		Last Modified: Tue, 03 Feb 2026 02:46:59 GMT  
		Size: 7.7 MB (7697007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684ede56bdd655ea395d6402abad1fd3eac9e0201c034e0691343d457a6c176`  
		Last Modified: Tue, 03 Feb 2026 02:47:00 GMT  
		Size: 46.0 MB (46008456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19660c80af566d8288cbcabe0acf8ab1ca9d08a24ed23eb0ac7e78f3126ae897`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c627e4d8997f8c3256237d0179ea8117ffc7d8e1d1bc114ab3739cb9fc041d`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71817e761f146bc0db938b7ff156402952733d18a1c61cfd5d401ba33c9c6afa`  
		Last Modified: Tue, 03 Feb 2026 02:46:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:05d2a0c6847d59833a934f1ad7b251d666bcb4f625272f8fd262fe1344374224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ac0b0a775664968df5de40e4e4e08242c360a7dedad6f3e37af952ab1691a`

```dockerfile
```

-	Layers:
	-	`sha256:b303c780ed0750f3941d3e4e158b39f3c5423c100764cf21ba9b2916b758e9a6`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3119a0176b2a5fd5be92bb563ab317458d1cf5a247e22c8a649e17d04db6f9`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9`

```console
$ docker pull chronograf@sha256:6bde6bedb800ff25d56a2138e23b1815c4f4a01ebb61520c9121607d21479fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.9` - linux; amd64

```console
$ docker pull chronograf@sha256:45aa7da8fd07c917f0b81b9229354f097ec81dbfc40d9e25bfbef2cfc0f72228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239fbd47e9acd33f72205fa2700b29a57b528c1b7defc3ab58e3ad54fe348b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d832a8b23bd03ee26616a22b1c1e726107955d2bb687b64d1abf55d80b9ef46`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 7.9 MB (7879833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0866d8ff3c769213e4f45f07b683ca8fbe9d3884d9550524c69cf8a9e0a14d0c`  
		Last Modified: Tue, 03 Feb 2026 02:43:57 GMT  
		Size: 48.9 MB (48867868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ca67b260ec18a154423f0bb4a80104a1fa46fcd4c081f87e39ebf4d49f8cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897073ceef77ec5ec1763d1ba23bf9c117ea150ac1d246acfce144bc41eb9a41`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f884f96a9a13252fe3683d44606dc301967a92be82099a04f4284840521d5d9`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:4186f1511d79fa944ef29f8288220efb49b030414016bffcdcc2a758cd529c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14086ce4dff01c2ae6810168e2dc833e98be020fb77101da309f97f5a31bea15`

```dockerfile
```

-	Layers:
	-	`sha256:96c0e54a1af2614a4429deb8fd8804388343d9294fcc6fca433f614084b582fc`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d54c1e3b5b8d8bcc4aff8c1e3090462fe76e012c2be268e35e3a55d4bb47c86`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:caacc6adbf2c4452766148b57d7999e190d5e1b879e600c8ae910a756cab9ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76790750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376ba31d0de7000782f5544cc1e6f54bfc40b5a09f2cf792ca5ceee9c0715cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:35:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 03:35:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:35:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:35:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:35:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb933aee84f3061780dc62fe2a11f8a092938c1f0128dc3e0cc478f20cae5f03`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 6.5 MB (6512172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d8f86617386920707c6dcb5bcfeaecd5519f37e0b72b40e6dc85634448615c`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 46.3 MB (46320011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b9281433f890ca914638da3dbe7a259675320d4141a66c3c2c5618d16cdae7`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94313802f27736d53e49c2875005d79d9778deef7bba174bb12e589caf4863`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eafeff883d8a20a4a4985fdc001c46d135191f83255afdf70f3ca85f39f5ee`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:d86d4ff611eba3aca600330c6a93b1ea23dfcffecd2dcab1e4fa74a6c800b572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb657b8dadf271f5de60a3a5bb024eda6f7a77168ea9f6ba6a593244123bc872`

```dockerfile
```

-	Layers:
	-	`sha256:5baf10006c61e2d5e257d76091f8f47dd1ca2973e1a47dd49f5e05d014e9c794`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b4b973bf15b61969d583df457b7db1bf4d323dc98aefb6114f6128a9a36999`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7c2925db5538718fe241a5ac3c233ef2112488a77d312ea9f4a9e83da0285565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81837759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fb1b21e6b2cb9ae6d9e52fc2d7e6bd1696d589c2c3f7a02d56d89fc5abd62e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:47 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:46:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73dec86f6dcfcd53df4db205f0e03292a615a504cc3cdd11a76253b1212154`  
		Last Modified: Tue, 03 Feb 2026 02:46:59 GMT  
		Size: 7.7 MB (7697007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684ede56bdd655ea395d6402abad1fd3eac9e0201c034e0691343d457a6c176`  
		Last Modified: Tue, 03 Feb 2026 02:47:00 GMT  
		Size: 46.0 MB (46008456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19660c80af566d8288cbcabe0acf8ab1ca9d08a24ed23eb0ac7e78f3126ae897`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c627e4d8997f8c3256237d0179ea8117ffc7d8e1d1bc114ab3739cb9fc041d`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71817e761f146bc0db938b7ff156402952733d18a1c61cfd5d401ba33c9c6afa`  
		Last Modified: Tue, 03 Feb 2026 02:46:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:05d2a0c6847d59833a934f1ad7b251d666bcb4f625272f8fd262fe1344374224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ac0b0a775664968df5de40e4e4e08242c360a7dedad6f3e37af952ab1691a`

```dockerfile
```

-	Layers:
	-	`sha256:b303c780ed0750f3941d3e4e158b39f3c5423c100764cf21ba9b2916b758e9a6`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3119a0176b2a5fd5be92bb563ab317458d1cf5a247e22c8a649e17d04db6f9`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9-alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:6de34a04b0787d95781986e6dc5623beb287e330b177ecd84f75606cbe445ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:53867133dfe648b2c7c3b78e1022ca2f6258d69682e4d026e8b41a1470292267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d4f964df130fd9037bbde7a8a4d8566cdf893ce3cd0f8edcd76505c388f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 02:43:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7830f3c8edd68a8536376a96eca428e237aabb292d096a2452935caf7d382290`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 4.2 MB (4209140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66e9053c810acbb3e09870bd9d18606cc5210206194aabf768de271ca4e54d`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 34.7 MB (34738488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5e6ecdb848e456edcf926ab5693567f2d8089fc14c37ec0bf4366e76737a8`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a9e67b4cecb96c3904448e95f7d7626086d1177ad02374c7375853df42f662`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40044839b1b7bd6a19a179311edb247a95a27b50e66771847335ee3355d21f6f`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:11717e304150636d10daa76841e5c0228c1c21f642922805b4d66c865d464dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbf9cfca557152f9d39254a2c7c141789e04c35cb1e726b3e2b0b443b6d6fd3`

```dockerfile
```

-	Layers:
	-	`sha256:65d32aaa8326f9dc0020b4adbaff20c595e511a4e087043b8f4eb14ae1b0da3e`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f192d33621b6168ce80d19562c8b896769e4c6ef5ed347479bf3056094d95ba3`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a1799957fd9519be7fa934508c07e723948ed7f46b4548a7269dbef4d60e1172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2593e2141b3bf383078bd6b4f8f71903c68dc84e2181f08471c1c5930036ce0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:32:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 03:32:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:32:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:32:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896896410843ab2b9183c49fcca34648fa92919572e197077ec52a471cac9cf2`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 3.5 MB (3511534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4431ad86132a51dd9b56273bddf8dd464bebe54554f6542ede559f1ce182c6d`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 33.1 MB (33097589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659d7c5c9496bfd2864251628545e5eb601ef79f2efc8c8240e75a151b11433d`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0780f68d2fed83dbdce686566a1e20b03d8a3ed8800901976815454e7f85959`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfad4b828128350cf7634fdebe89a4370216d63b916bec048c0c26aa6609a3d`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:79fb52c003a09a3d30ba5cedfe4d4bd49bc3d1fbf02f2d61f8b5f16ba5e9c4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fcf2b580bd56cd18c4cc266b1f1af87e9070c8814fa02a885c475bdf5902cb`

```dockerfile
```

-	Layers:
	-	`sha256:f9b5d9a4118c355b47e9ecb7c6c662a0c4bfadbd19b774a28970ec9831a1ecd4`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d978b77cbdf0d3f871781926f655717b9442a8af1f99152eb7f7c1bd0aa157bd`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5e10c6916369bcd5955297b57ee0c9b2bd8e5e439360907ce9040e299ad0cd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66217358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10d6fda72e468ad43f642abf68e11692b9ba0c00175c1730e0422df2a409ef0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:46:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 02:46:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f582e96274d7290cdb140e375aec265cac526b9ebc0beaf2cd224ae33ae3a`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 4.2 MB (4210372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634f033955d068cf3438464898ac018f06ad5d565304ac5a55561068fc1359a9`  
		Last Modified: Tue, 03 Feb 2026 02:46:29 GMT  
		Size: 33.2 MB (33238153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb015ee5b321982a725e0d2561c905305d7728062bba1a3de14b8a1c86855ad`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49b1737daa292d38624283c864fde14e2d16bcf1d7dbd6ab5ce99b6fe1a715c`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a56ac031c186d743e01a711436fa7a3b8fd967f0e16e6c862f24b92bbc85a3c`  
		Last Modified: Tue, 03 Feb 2026 02:46:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:87a97767af673f54dec03990d852bee2695c22f2a364e431fe294554b6a4a903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3649cbb999b026ac458dc87625a1f3465b2d80df116731abce09e76841985e`

```dockerfile
```

-	Layers:
	-	`sha256:6ef3ba2a645dcaf7aef025ef777c22504f6f51be3c220515c259a63d8536df85`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3dc1d086a9c66bb14f93f702752bb8f2d442894e1b2b927a7f3cbfa79fac49`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:64bef3719ffd40e750e40a39da4c12abaa87dfb5feb5eda538abf94e3accb618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3f189f37cc38433df9fbac676c503a10acef7c7614624600135f250066886161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bec3fa8c5026e398c27b75bfa769e7655e34f7170bcdc9037dac726934f2ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 28 Jan 2026 02:53:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:53:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:53:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:53:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340aae68687d2116364c9e894fd45843e9743365d10615f35ce86ed559892f63`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 19.6 MB (19556564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c53db3e00d80e1eb53e2db543c42e48bbe8cedbd46305f512e93b6a97dca45`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dcdc4fbf054e697ef5ae3221a5d4fd5e2fdd105c6d4ff0de12003ee0b27b30`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda149c9eaf485c096f2594f2e965917ccbc4373f09c74334e243c6b695c21c`  
		Last Modified: Wed, 28 Jan 2026 02:53:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c56020b83aeb19cda9433c13248182ca3b3227bdfea0e3e87429fa828fce4e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f387fa3c690e841ea63c593cf9ab0ea8833159bbd96572eb1480d58af1824f1`

```dockerfile
```

-	Layers:
	-	`sha256:3952b13f0b8499685ee3fd998a70ea826c97a65c6f328d3185fff832bf3bfd8a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7be3070420c927548a22fb90dc77dcced4eaf6f13c2cb97512b1fbff884e9e`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:6de34a04b0787d95781986e6dc5623beb287e330b177ecd84f75606cbe445ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:53867133dfe648b2c7c3b78e1022ca2f6258d69682e4d026e8b41a1470292267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d4f964df130fd9037bbde7a8a4d8566cdf893ce3cd0f8edcd76505c388f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 02:43:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7830f3c8edd68a8536376a96eca428e237aabb292d096a2452935caf7d382290`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 4.2 MB (4209140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66e9053c810acbb3e09870bd9d18606cc5210206194aabf768de271ca4e54d`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 34.7 MB (34738488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5e6ecdb848e456edcf926ab5693567f2d8089fc14c37ec0bf4366e76737a8`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a9e67b4cecb96c3904448e95f7d7626086d1177ad02374c7375853df42f662`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40044839b1b7bd6a19a179311edb247a95a27b50e66771847335ee3355d21f6f`  
		Last Modified: Tue, 03 Feb 2026 02:43:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:11717e304150636d10daa76841e5c0228c1c21f642922805b4d66c865d464dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbf9cfca557152f9d39254a2c7c141789e04c35cb1e726b3e2b0b443b6d6fd3`

```dockerfile
```

-	Layers:
	-	`sha256:65d32aaa8326f9dc0020b4adbaff20c595e511a4e087043b8f4eb14ae1b0da3e`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f192d33621b6168ce80d19562c8b896769e4c6ef5ed347479bf3056094d95ba3`  
		Last Modified: Tue, 03 Feb 2026 02:43:35 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a1799957fd9519be7fa934508c07e723948ed7f46b4548a7269dbef4d60e1172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2593e2141b3bf383078bd6b4f8f71903c68dc84e2181f08471c1c5930036ce0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:32:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 03:32:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:32:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:32:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:32:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:32:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896896410843ab2b9183c49fcca34648fa92919572e197077ec52a471cac9cf2`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 3.5 MB (3511534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4431ad86132a51dd9b56273bddf8dd464bebe54554f6542ede559f1ce182c6d`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 33.1 MB (33097589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659d7c5c9496bfd2864251628545e5eb601ef79f2efc8c8240e75a151b11433d`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0780f68d2fed83dbdce686566a1e20b03d8a3ed8800901976815454e7f85959`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfad4b828128350cf7634fdebe89a4370216d63b916bec048c0c26aa6609a3d`  
		Last Modified: Tue, 03 Feb 2026 03:33:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:79fb52c003a09a3d30ba5cedfe4d4bd49bc3d1fbf02f2d61f8b5f16ba5e9c4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fcf2b580bd56cd18c4cc266b1f1af87e9070c8814fa02a885c475bdf5902cb`

```dockerfile
```

-	Layers:
	-	`sha256:f9b5d9a4118c355b47e9ecb7c6c662a0c4bfadbd19b774a28970ec9831a1ecd4`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d978b77cbdf0d3f871781926f655717b9442a8af1f99152eb7f7c1bd0aa157bd`  
		Last Modified: Tue, 03 Feb 2026 03:33:08 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5e10c6916369bcd5955297b57ee0c9b2bd8e5e439360907ce9040e299ad0cd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66217358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10d6fda72e468ad43f642abf68e11692b9ba0c00175c1730e0422df2a409ef0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:46:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 03 Feb 2026 02:46:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f582e96274d7290cdb140e375aec265cac526b9ebc0beaf2cd224ae33ae3a`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 4.2 MB (4210372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634f033955d068cf3438464898ac018f06ad5d565304ac5a55561068fc1359a9`  
		Last Modified: Tue, 03 Feb 2026 02:46:29 GMT  
		Size: 33.2 MB (33238153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb015ee5b321982a725e0d2561c905305d7728062bba1a3de14b8a1c86855ad`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49b1737daa292d38624283c864fde14e2d16bcf1d7dbd6ab5ce99b6fe1a715c`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a56ac031c186d743e01a711436fa7a3b8fd967f0e16e6c862f24b92bbc85a3c`  
		Last Modified: Tue, 03 Feb 2026 02:46:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:87a97767af673f54dec03990d852bee2695c22f2a364e431fe294554b6a4a903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3649cbb999b026ac458dc87625a1f3465b2d80df116731abce09e76841985e`

```dockerfile
```

-	Layers:
	-	`sha256:6ef3ba2a645dcaf7aef025ef777c22504f6f51be3c220515c259a63d8536df85`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3dc1d086a9c66bb14f93f702752bb8f2d442894e1b2b927a7f3cbfa79fac49`  
		Last Modified: Tue, 03 Feb 2026 02:46:28 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:64bef3719ffd40e750e40a39da4c12abaa87dfb5feb5eda538abf94e3accb618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3f189f37cc38433df9fbac676c503a10acef7c7614624600135f250066886161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bec3fa8c5026e398c27b75bfa769e7655e34f7170bcdc9037dac726934f2ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 28 Jan 2026 02:53:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:53:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:53:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:53:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340aae68687d2116364c9e894fd45843e9743365d10615f35ce86ed559892f63`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 19.6 MB (19556564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c53db3e00d80e1eb53e2db543c42e48bbe8cedbd46305f512e93b6a97dca45`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dcdc4fbf054e697ef5ae3221a5d4fd5e2fdd105c6d4ff0de12003ee0b27b30`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda149c9eaf485c096f2594f2e965917ccbc4373f09c74334e243c6b695c21c`  
		Last Modified: Wed, 28 Jan 2026 02:53:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c56020b83aeb19cda9433c13248182ca3b3227bdfea0e3e87429fa828fce4e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f387fa3c690e841ea63c593cf9ab0ea8833159bbd96572eb1480d58af1824f1`

```dockerfile
```

-	Layers:
	-	`sha256:3952b13f0b8499685ee3fd998a70ea826c97a65c6f328d3185fff832bf3bfd8a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7be3070420c927548a22fb90dc77dcced4eaf6f13c2cb97512b1fbff884e9e`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:afb56af1ec04127a0150da23439620bae240b3131f79493639a5e495373f7136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:82a431f61c4d69afd5180b27e1bdc57a50393935607e215f7a38af8aabed59a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a739890f78def91defebb181a3dd344b42842180933110d985a1f5853a594a43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 02:43:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:27 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9b8171691d530d3ec2f27a2155d2036234c78d2f3acbb666976a0d1a294f9`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 5.2 MB (5224154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90df1e0931fad7a130653cd382b06b9f20689a1b6b77234e063269a0e35fde2a`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 34.4 MB (34364287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c30d02512d9ff1c445a959442491ed5f80b9ceb4b07032660fa609f5f213`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954cdfd15de94c8c186393557c201820de686e916ee1c20a9154a1ad694697a2`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fdf76f1a2da10f860fb25fb56a712100a150a0f05dc1896b9bbda93eb2d214`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b08e298e576c3f079b070532e8989143d503241bbb24614a7721689685b8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf266c526cd82086229ebfa08307d139ef95fdc5e1ecdd89c00ad11870415b`

```dockerfile
```

-	Layers:
	-	`sha256:9db2c35606289e7a65ada290859169801b1965cc1f1bbffedcd68adfbef8cdde`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ac23ac6af04d5746f05ee970ad5655dee9161ebccb784c3107075e32e41cbb`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:336188c960b148a90e6cb26ebcb49cf0e3789110954d31e0c790c4bb16bf7632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361f2fab94326829236e1a8d8ae3eb0c6b8a87a480e54120b858cb5fb5cab29c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:33:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 03:34:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:34:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:34:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:34:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6688841d28732325dfa5be8b6ae5b3d73d091ee2db7fd0e2c3192063771d50`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 4.5 MB (4489811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abf34edd7b6734e2545e6c9ef59dda3376a3112285b8cd63f28ac100a54ef78`  
		Last Modified: Tue, 03 Feb 2026 03:34:12 GMT  
		Size: 32.5 MB (32534934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e42b0ec62682fa25bd9ae946eb4a4bd3108052f3ddf63e14e0204eaa221c32`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afccf8853fba24eaddcabe219182955f1a075304cca7242749a85b27d9ac521b`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186b078224833e7b0d84db431649a90c26edc2f1d6ef1955a94e65b140c562e`  
		Last Modified: Tue, 03 Feb 2026 03:34:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:a5dc6ea7d8493b46fe94378010301b55d747e15199b5d40687af575baddb9687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b261a2aaa9104201b622fcfcae77a15d66a7660c932abaafe6039f38208a40`

```dockerfile
```

-	Layers:
	-	`sha256:1fb5543612ab28fd6e2add3310b093ee795fa2a1189872cad2e20c8e84586cf8`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4157936f1d2dc51d2250b2fe1d657d059ba9de63143aa34be890edff24965cb6`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e0dfd94c604bdbbe5137018cddd1e413c0a9e24e7d6f8df2869fc643833e1a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66406144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b1e31c7867b1e30e6f4f3eebaffbd3c534d3f33d0c6ced5b80788535ec1639`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:46:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 02:46:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7d04997c54344d1b2b31f83e82a504889027e083ccfd66ccea5d739e66101b`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 5.2 MB (5207807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d991eceedd5871ce49507dfe240ca861b2b543e39752857948340f04239c865`  
		Last Modified: Tue, 03 Feb 2026 02:46:38 GMT  
		Size: 32.4 MB (32429496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6610b67fd2a917edeb723aa61aa992df5dd7927a786445c1e28254aa66036f2f`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fe233f21e916bf527e76a1a36701cfbecf3ab1332330f7042429608f68ff95`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b083ffe31a631618db6441f44273fe78f69936895945d29e9debcccd71982673`  
		Last Modified: Tue, 03 Feb 2026 02:46:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:90b415661e24b308de3d54d99d0e91b675a94303f97c6cd807e284767c7e09e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16deeb8df141c64002e99c04aa2aa8e2fdc16f10c7b6bfac4d6b129ef23f61e`

```dockerfile
```

-	Layers:
	-	`sha256:dc149fed92c7c71599ef401bf66b68b0f5914c1707105d88ecf28a3948bcb664`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58586e4315c4e195146754024800b84957dcd98d73b81b6b9e9e17a21428f322`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:eaa3bb3ccb8ee814154bf133b1f66211d509c29f6dd1e1526c10230e208b863c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c2bf30f869435c0b92e73e5d840baecf10b7556dee1180eab812a2e5c64ee8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2dae78c59d8c5be31f4f138985d18bd1ba2aeb87bccc37c803d766d4dfb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:54:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 28 Jan 2026 02:54:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:54:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:54:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11511055c1a92ee4826f4450c606b4c6fe01663551c2520901ee8904c7cc029e`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e7cced7996c2c54d3705c37d6189dd45203311e86f379e19dac56c87d79c1`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 290.8 KB (290775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85e7552262500b34023157ef8b78d59c9f8aecf673d089df4240d9c9410eaf`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 19.2 MB (19204012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f59d04c053bed8109181709b7b72268373c858113d4d325f91a61c9860fe15`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39810aef4e0fd17cd3dd3a5c3df656a78821f4433c31d84d22a70687f39fc8`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39803bc8b4320a837d54074da9cd5a373b5492fbb69ba833e15e82cb22d38c2e`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8db07f0161f7cd63e13b7a8ec9f585002560d6c1aeb6bf3bfe117e6023c60030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f169dc8bb776368bcf6aeabb508e8f02347ed3c83e3ce9438f29a553783f718`

```dockerfile
```

-	Layers:
	-	`sha256:2a4f2a2d49e087fc0c9683afc43c5a8338ed6ca288ed80700190e6600854103b`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94417dbea42e77a238ff18ac37fde210a7fb42d1a5ba372bd1e9e6e02f0e3f2d`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:afb56af1ec04127a0150da23439620bae240b3131f79493639a5e495373f7136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:82a431f61c4d69afd5180b27e1bdc57a50393935607e215f7a38af8aabed59a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a739890f78def91defebb181a3dd344b42842180933110d985a1f5853a594a43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 02:43:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:27 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9b8171691d530d3ec2f27a2155d2036234c78d2f3acbb666976a0d1a294f9`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 5.2 MB (5224154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90df1e0931fad7a130653cd382b06b9f20689a1b6b77234e063269a0e35fde2a`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 34.4 MB (34364287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c30d02512d9ff1c445a959442491ed5f80b9ceb4b07032660fa609f5f213`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954cdfd15de94c8c186393557c201820de686e916ee1c20a9154a1ad694697a2`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fdf76f1a2da10f860fb25fb56a712100a150a0f05dc1896b9bbda93eb2d214`  
		Last Modified: Tue, 03 Feb 2026 02:43:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b08e298e576c3f079b070532e8989143d503241bbb24614a7721689685b8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf266c526cd82086229ebfa08307d139ef95fdc5e1ecdd89c00ad11870415b`

```dockerfile
```

-	Layers:
	-	`sha256:9db2c35606289e7a65ada290859169801b1965cc1f1bbffedcd68adfbef8cdde`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ac23ac6af04d5746f05ee970ad5655dee9161ebccb784c3107075e32e41cbb`  
		Last Modified: Tue, 03 Feb 2026 02:43:37 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:336188c960b148a90e6cb26ebcb49cf0e3789110954d31e0c790c4bb16bf7632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361f2fab94326829236e1a8d8ae3eb0c6b8a87a480e54120b858cb5fb5cab29c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:33:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 03:34:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:34:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:34:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:34:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:34:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6688841d28732325dfa5be8b6ae5b3d73d091ee2db7fd0e2c3192063771d50`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 4.5 MB (4489811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abf34edd7b6734e2545e6c9ef59dda3376a3112285b8cd63f28ac100a54ef78`  
		Last Modified: Tue, 03 Feb 2026 03:34:12 GMT  
		Size: 32.5 MB (32534934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e42b0ec62682fa25bd9ae946eb4a4bd3108052f3ddf63e14e0204eaa221c32`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afccf8853fba24eaddcabe219182955f1a075304cca7242749a85b27d9ac521b`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2186b078224833e7b0d84db431649a90c26edc2f1d6ef1955a94e65b140c562e`  
		Last Modified: Tue, 03 Feb 2026 03:34:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a5dc6ea7d8493b46fe94378010301b55d747e15199b5d40687af575baddb9687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b261a2aaa9104201b622fcfcae77a15d66a7660c932abaafe6039f38208a40`

```dockerfile
```

-	Layers:
	-	`sha256:1fb5543612ab28fd6e2add3310b093ee795fa2a1189872cad2e20c8e84586cf8`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4157936f1d2dc51d2250b2fe1d657d059ba9de63143aa34be890edff24965cb6`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e0dfd94c604bdbbe5137018cddd1e413c0a9e24e7d6f8df2869fc643833e1a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66406144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b1e31c7867b1e30e6f4f3eebaffbd3c534d3f33d0c6ced5b80788535ec1639`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:46:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 03 Feb 2026 02:46:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7d04997c54344d1b2b31f83e82a504889027e083ccfd66ccea5d739e66101b`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 5.2 MB (5207807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d991eceedd5871ce49507dfe240ca861b2b543e39752857948340f04239c865`  
		Last Modified: Tue, 03 Feb 2026 02:46:38 GMT  
		Size: 32.4 MB (32429496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6610b67fd2a917edeb723aa61aa992df5dd7927a786445c1e28254aa66036f2f`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fe233f21e916bf527e76a1a36701cfbecf3ab1332330f7042429608f68ff95`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b083ffe31a631618db6441f44273fe78f69936895945d29e9debcccd71982673`  
		Last Modified: Tue, 03 Feb 2026 02:46:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:90b415661e24b308de3d54d99d0e91b675a94303f97c6cd807e284767c7e09e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16deeb8df141c64002e99c04aa2aa8e2fdc16f10c7b6bfac4d6b129ef23f61e`

```dockerfile
```

-	Layers:
	-	`sha256:dc149fed92c7c71599ef401bf66b68b0f5914c1707105d88ecf28a3948bcb664`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58586e4315c4e195146754024800b84957dcd98d73b81b6b9e9e17a21428f322`  
		Last Modified: Tue, 03 Feb 2026 02:46:37 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:eaa3bb3ccb8ee814154bf133b1f66211d509c29f6dd1e1526c10230e208b863c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c2bf30f869435c0b92e73e5d840baecf10b7556dee1180eab812a2e5c64ee8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2dae78c59d8c5be31f4f138985d18bd1ba2aeb87bccc37c803d766d4dfb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:54:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 28 Jan 2026 02:54:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:54:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:54:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11511055c1a92ee4826f4450c606b4c6fe01663551c2520901ee8904c7cc029e`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e7cced7996c2c54d3705c37d6189dd45203311e86f379e19dac56c87d79c1`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 290.8 KB (290775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85e7552262500b34023157ef8b78d59c9f8aecf673d089df4240d9c9410eaf`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 19.2 MB (19204012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f59d04c053bed8109181709b7b72268373c858113d4d325f91a61c9860fe15`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39810aef4e0fd17cd3dd3a5c3df656a78821f4433c31d84d22a70687f39fc8`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39803bc8b4320a837d54074da9cd5a373b5492fbb69ba833e15e82cb22d38c2e`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8db07f0161f7cd63e13b7a8ec9f585002560d6c1aeb6bf3bfe117e6023c60030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f169dc8bb776368bcf6aeabb508e8f02347ed3c83e3ce9438f29a553783f718`

```dockerfile
```

-	Layers:
	-	`sha256:2a4f2a2d49e087fc0c9683afc43c5a8338ed6ca288ed80700190e6600854103b`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94417dbea42e77a238ff18ac37fde210a7fb42d1a5ba372bd1e9e6e02f0e3f2d`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:b6d3dc470eaf758a513fe1782c12c4e1fc27a4d61332f0aac024a9f6d1763e24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:a45e8e64d17f42b9e9c279d0bf1889ebf89fe35e7b882a08570dd98508a15db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4655efdd675a0a75671ce01aae0092e1ce6877121979aabc54172c30f42ad03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5e4ec153d6920bdebb6be24cc5f807661e4f3adb033edef894113c413037d6`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 5.2 MB (5224176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c284b94cdb59a4c9f31ec37144def8dca26a6907aa120f44967ce78d01125428`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 35.0 MB (35011750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e57fc5618b979d68cdb22944bd81fff63de924b1f91e15151954cf9d8f1069e`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9d94951f3496996faf5f42759f12fe7851be9b9b24a5f2b4e130a03650f2c1`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b850e1d1f2d903e380c18a4a04a63c8e3b87f9b924fb8832125159099f68807d`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:03162ca1a28f4b4bce87866220c4efe3bf401d8fa619f8a4aa9cca1ee8981749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b8c3f4b49842e602eec2744868cbffb208b6e6d7efd1c46a712ff827660c1`

```dockerfile
```

-	Layers:
	-	`sha256:bd4cf9cd526f7bddb59f10de49d132869fcccdf36a27fc22df67a6750e7efeb5`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddcad924cd9928d89fa886b12280a937645f1ef9f1643edd90a25e00273a917`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c61736c271adbf6830d2a6bd4ebd6dd8736e0e91cbba229d7021938920d1e80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63371919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023addcee356f26dae4a11d1a4a4f54f31dca33b8678986f64663c5c9010c656`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:33:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 03:34:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:34:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:34:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:34:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6688841d28732325dfa5be8b6ae5b3d73d091ee2db7fd0e2c3192063771d50`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 4.5 MB (4489811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e866dd9190784772c2280cc2405468303aac4cc414d42cbab37798278929e7`  
		Last Modified: Tue, 03 Feb 2026 03:34:34 GMT  
		Size: 33.3 MB (33311614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d68fdf5580115a2b6233dcc4bf69a6da9a9444022bd8b9bbd1aef488f3915`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78262b4b0bd299c09e7e01138074e4a965fdcb8041533663fc0b45e16a67bab4`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd375493299e95fc6da871fcfb852dbda3e2a7db139e00bd3854318195b956d`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:e5ca84eb6a4f1476344dd01fc9f98c7a3a8d838b0dfdbca324e2f7dadc79c679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64213e9607440d6caf2c5321aca6054685ae1f4115138a4d3c128595d0afc5f7`

```dockerfile
```

-	Layers:
	-	`sha256:47f84c5f5ed53f6481cba830141f842a343f6befb686d343fc5ab6ff81dd7d7f`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea0d6f8d9a81db7ee18fd3cb04f1b09a7afa05b01aa00a7eb8672a5a4ae5267`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:58fcfe1b453ecc08288c2d18ddf48cf96a92f63f1c857890792b80888728dd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67158910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bb8d93dbe0c1f9c0ce88e617528e5de580cc859103aed65c190a665db06664`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:46:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 02:46:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d115b551e86982ddd43b793306dd6e2ac2218998d9425e0f1b7c7f143d55b4`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 5.2 MB (5207830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fc0a5391b98afc67b16212ae6e7af4b3c9647968c642549c9b31b85ddced93`  
		Last Modified: Tue, 03 Feb 2026 02:46:41 GMT  
		Size: 33.2 MB (33182248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c5be6da4812c0cd64515bf48d86608457b3b4cde2474f007a6bd4a568be942`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bc01cee2383e14093adb21cf89e331d1c264ea5101107d21c1ada05cc75efe`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b083ffe31a631618db6441f44273fe78f69936895945d29e9debcccd71982673`  
		Last Modified: Tue, 03 Feb 2026 02:46:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:6b66c5ca0d5dc55db561e2477187433f2c415193efe7eaf1dcc54c49050dd93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1dbe4e4e8c376a6ee4b050c5e20601776d00fc760731dd32bf625a8a32a7273`

```dockerfile
```

-	Layers:
	-	`sha256:70dec37df0e70a26030b5a7432f76a71b3ffc9b6d6830cdd1e92befff31ac1af`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73be463a2fc6c168f548066ef499a76bdbb1282cfeb8f324d5b185e4c7e7efab`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:fe4e3b3c10a641ad805b9ce0ec78cda2f470f49a830894c722953c8fb728fcb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:67cedab187e8fc183d786cf2258d4005ec583930cc20e74da6812a9e7ff42a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23615399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f6aa3073f13adbf88c9cccbd9ab0fbb58be572d0f96c9e48d3d49e2b1b015`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 28 Jan 2026 02:55:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49502ea6fb236afee58c16f44002da47fa15e3106a666c8b493bb26052c9274a`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 19.7 MB (19672093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21543e57ca18bdf7a24a618747db1a314a907889b35e10bf5d53278ef3419640`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac25ca50f9519d41319a760291be5f082cfa992b201b65d9f8ce0852c6735c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579664805c4fdab94b0811a476f26cd0ce412bc8c0c5a0bab5ecbdba4b190a7d`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b3df4976cd08554c6148388fc472cd29690db4573063bd6d7675893a2756bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af162ec484f5c5e51d9958dc581b210cf6055821574b4630fdb8d5c27c93cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:e1fda32b72505ea72431129c688691bca18d6a71dfc54ac36b83c1657128e64c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8be116a02c551af1fa72b7f056c9711e39f115b000563402cba9f992d61ff`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:b6d3dc470eaf758a513fe1782c12c4e1fc27a4d61332f0aac024a9f6d1763e24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:a45e8e64d17f42b9e9c279d0bf1889ebf89fe35e7b882a08570dd98508a15db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4655efdd675a0a75671ce01aae0092e1ce6877121979aabc54172c30f42ad03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:43:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5e4ec153d6920bdebb6be24cc5f807661e4f3adb033edef894113c413037d6`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 5.2 MB (5224176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c284b94cdb59a4c9f31ec37144def8dca26a6907aa120f44967ce78d01125428`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 35.0 MB (35011750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e57fc5618b979d68cdb22944bd81fff63de924b1f91e15151954cf9d8f1069e`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9d94951f3496996faf5f42759f12fe7851be9b9b24a5f2b4e130a03650f2c1`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b850e1d1f2d903e380c18a4a04a63c8e3b87f9b924fb8832125159099f68807d`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:03162ca1a28f4b4bce87866220c4efe3bf401d8fa619f8a4aa9cca1ee8981749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b8c3f4b49842e602eec2744868cbffb208b6e6d7efd1c46a712ff827660c1`

```dockerfile
```

-	Layers:
	-	`sha256:bd4cf9cd526f7bddb59f10de49d132869fcccdf36a27fc22df67a6750e7efeb5`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddcad924cd9928d89fa886b12280a937645f1ef9f1643edd90a25e00273a917`  
		Last Modified: Tue, 03 Feb 2026 02:43:54 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c61736c271adbf6830d2a6bd4ebd6dd8736e0e91cbba229d7021938920d1e80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63371919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023addcee356f26dae4a11d1a4a4f54f31dca33b8678986f64663c5c9010c656`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:33:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 03:34:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:34:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:34:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:34:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:34:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6688841d28732325dfa5be8b6ae5b3d73d091ee2db7fd0e2c3192063771d50`  
		Last Modified: Tue, 03 Feb 2026 03:34:11 GMT  
		Size: 4.5 MB (4489811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e866dd9190784772c2280cc2405468303aac4cc414d42cbab37798278929e7`  
		Last Modified: Tue, 03 Feb 2026 03:34:34 GMT  
		Size: 33.3 MB (33311614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d68fdf5580115a2b6233dcc4bf69a6da9a9444022bd8b9bbd1aef488f3915`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78262b4b0bd299c09e7e01138074e4a965fdcb8041533663fc0b45e16a67bab4`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd375493299e95fc6da871fcfb852dbda3e2a7db139e00bd3854318195b956d`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:e5ca84eb6a4f1476344dd01fc9f98c7a3a8d838b0dfdbca324e2f7dadc79c679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64213e9607440d6caf2c5321aca6054685ae1f4115138a4d3c128595d0afc5f7`

```dockerfile
```

-	Layers:
	-	`sha256:47f84c5f5ed53f6481cba830141f842a343f6befb686d343fc5ab6ff81dd7d7f`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea0d6f8d9a81db7ee18fd3cb04f1b09a7afa05b01aa00a7eb8672a5a4ae5267`  
		Last Modified: Tue, 03 Feb 2026 03:34:33 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:58fcfe1b453ecc08288c2d18ddf48cf96a92f63f1c857890792b80888728dd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67158910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bb8d93dbe0c1f9c0ce88e617528e5de580cc859103aed65c190a665db06664`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:46:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 03 Feb 2026 02:46:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d115b551e86982ddd43b793306dd6e2ac2218998d9425e0f1b7c7f143d55b4`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 5.2 MB (5207830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fc0a5391b98afc67b16212ae6e7af4b3c9647968c642549c9b31b85ddced93`  
		Last Modified: Tue, 03 Feb 2026 02:46:41 GMT  
		Size: 33.2 MB (33182248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c5be6da4812c0cd64515bf48d86608457b3b4cde2474f007a6bd4a568be942`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bc01cee2383e14093adb21cf89e331d1c264ea5101107d21c1ada05cc75efe`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b083ffe31a631618db6441f44273fe78f69936895945d29e9debcccd71982673`  
		Last Modified: Tue, 03 Feb 2026 02:46:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:6b66c5ca0d5dc55db561e2477187433f2c415193efe7eaf1dcc54c49050dd93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1dbe4e4e8c376a6ee4b050c5e20601776d00fc760731dd32bf625a8a32a7273`

```dockerfile
```

-	Layers:
	-	`sha256:70dec37df0e70a26030b5a7432f76a71b3ffc9b6d6830cdd1e92befff31ac1af`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73be463a2fc6c168f548066ef499a76bdbb1282cfeb8f324d5b185e4c7e7efab`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:fe4e3b3c10a641ad805b9ce0ec78cda2f470f49a830894c722953c8fb728fcb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:67cedab187e8fc183d786cf2258d4005ec583930cc20e74da6812a9e7ff42a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23615399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f6aa3073f13adbf88c9cccbd9ab0fbb58be572d0f96c9e48d3d49e2b1b015`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 28 Jan 2026 02:55:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49502ea6fb236afee58c16f44002da47fa15e3106a666c8b493bb26052c9274a`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 19.7 MB (19672093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21543e57ca18bdf7a24a618747db1a314a907889b35e10bf5d53278ef3419640`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac25ca50f9519d41319a760291be5f082cfa992b201b65d9f8ce0852c6735c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579664805c4fdab94b0811a476f26cd0ce412bc8c0c5a0bab5ecbdba4b190a7d`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b3df4976cd08554c6148388fc472cd29690db4573063bd6d7675893a2756bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af162ec484f5c5e51d9958dc581b210cf6055821574b4630fdb8d5c27c93cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:e1fda32b72505ea72431129c688691bca18d6a71dfc54ac36b83c1657128e64c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8be116a02c551af1fa72b7f056c9711e39f115b000563402cba9f992d61ff`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:6bde6bedb800ff25d56a2138e23b1815c4f4a01ebb61520c9121607d21479fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:45aa7da8fd07c917f0b81b9229354f097ec81dbfc40d9e25bfbef2cfc0f72228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85000652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239fbd47e9acd33f72205fa2700b29a57b528c1b7defc3ab58e3ad54fe348b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:43:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:43:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:43:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:43:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:43:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:43:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d832a8b23bd03ee26616a22b1c1e726107955d2bb687b64d1abf55d80b9ef46`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 7.9 MB (7879833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0866d8ff3c769213e4f45f07b683ca8fbe9d3884d9550524c69cf8a9e0a14d0c`  
		Last Modified: Tue, 03 Feb 2026 02:43:57 GMT  
		Size: 48.9 MB (48867868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ca67b260ec18a154423f0bb4a80104a1fa46fcd4c081f87e39ebf4d49f8cc`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897073ceef77ec5ec1763d1ba23bf9c117ea150ac1d246acfce144bc41eb9a41`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f884f96a9a13252fe3683d44606dc301967a92be82099a04f4284840521d5d9`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:4186f1511d79fa944ef29f8288220efb49b030414016bffcdcc2a758cd529c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14086ce4dff01c2ae6810168e2dc833e98be020fb77101da309f97f5a31bea15`

```dockerfile
```

-	Layers:
	-	`sha256:96c0e54a1af2614a4429deb8fd8804388343d9294fcc6fca433f614084b582fc`  
		Last Modified: Tue, 03 Feb 2026 02:43:56 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d54c1e3b5b8d8bcc4aff8c1e3090462fe76e012c2be268e35e3a55d4bb47c86`  
		Last Modified: Tue, 03 Feb 2026 02:43:55 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:caacc6adbf2c4452766148b57d7999e190d5e1b879e600c8ae910a756cab9ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76790750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376ba31d0de7000782f5544cc1e6f54bfc40b5a09f2cf792ca5ceee9c0715cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:35:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 03:35:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 03:35:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 03:35:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:35:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:35:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb933aee84f3061780dc62fe2a11f8a092938c1f0128dc3e0cc478f20cae5f03`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 6.5 MB (6512172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d8f86617386920707c6dcb5bcfeaecd5519f37e0b72b40e6dc85634448615c`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 46.3 MB (46320011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b9281433f890ca914638da3dbe7a259675320d4141a66c3c2c5618d16cdae7`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94313802f27736d53e49c2875005d79d9778deef7bba174bb12e589caf4863`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eafeff883d8a20a4a4985fdc001c46d135191f83255afdf70f3ca85f39f5ee`  
		Last Modified: Tue, 03 Feb 2026 03:35:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d86d4ff611eba3aca600330c6a93b1ea23dfcffecd2dcab1e4fa74a6c800b572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb657b8dadf271f5de60a3a5bb024eda6f7a77168ea9f6ba6a593244123bc872`

```dockerfile
```

-	Layers:
	-	`sha256:5baf10006c61e2d5e257d76091f8f47dd1ca2973e1a47dd49f5e05d014e9c794`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b4b973bf15b61969d583df457b7db1bf4d323dc98aefb6114f6128a9a36999`  
		Last Modified: Tue, 03 Feb 2026 03:35:28 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7c2925db5538718fe241a5ac3c233ef2112488a77d312ea9f4a9e83da0285565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81837759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fb1b21e6b2cb9ae6d9e52fc2d7e6bd1696d589c2c3f7a02d56d89fc5abd62e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 02:46:47 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 03 Feb 2026 02:46:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 03 Feb 2026 02:46:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 03 Feb 2026 02:46:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 02:46:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73dec86f6dcfcd53df4db205f0e03292a615a504cc3cdd11a76253b1212154`  
		Last Modified: Tue, 03 Feb 2026 02:46:59 GMT  
		Size: 7.7 MB (7697007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684ede56bdd655ea395d6402abad1fd3eac9e0201c034e0691343d457a6c176`  
		Last Modified: Tue, 03 Feb 2026 02:47:00 GMT  
		Size: 46.0 MB (46008456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19660c80af566d8288cbcabe0acf8ab1ca9d08a24ed23eb0ac7e78f3126ae897`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c627e4d8997f8c3256237d0179ea8117ffc7d8e1d1bc114ab3739cb9fc041d`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71817e761f146bc0db938b7ff156402952733d18a1c61cfd5d401ba33c9c6afa`  
		Last Modified: Tue, 03 Feb 2026 02:46:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:05d2a0c6847d59833a934f1ad7b251d666bcb4f625272f8fd262fe1344374224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83ac0b0a775664968df5de40e4e4e08242c360a7dedad6f3e37af952ab1691a`

```dockerfile
```

-	Layers:
	-	`sha256:b303c780ed0750f3941d3e4e158b39f3c5423c100764cf21ba9b2916b758e9a6`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3119a0176b2a5fd5be92bb563ab317458d1cf5a247e22c8a649e17d04db6f9`  
		Last Modified: Tue, 03 Feb 2026 02:46:58 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
