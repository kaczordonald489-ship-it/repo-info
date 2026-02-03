<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.1`](#telegraf1371)
-	[`telegraf:1.37.1-alpine`](#telegraf1371-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:a30facfc4c52ffe93d7dacff73cda1dc22aa75930f5f8153c0bf6fb7a3068fec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35` - linux; amd64

```console
$ docker pull telegraf@sha256:993f35a9701d19adb4307f93239f5714f58e7960104c4f32d05ae61ca4d45866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171040750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb816d6824a287813e71886bfb01d700431acfada0dbb64d665c11fa57e2de6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:42:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 03 Feb 2026 03:42:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:42:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:42:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:42:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cb6409cdbe5467f35f1e3af1f88ce3933242a9c8b47f40d03df4050a55b92f`  
		Last Modified: Tue, 03 Feb 2026 03:42:25 GMT  
		Size: 18.9 MB (18944427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940ef600ddcf6d55097765a9f871acc42e3e0a63d1db450b877a1278814ebc9a`  
		Last Modified: Tue, 03 Feb 2026 03:42:24 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc279bbe89fbc3b5468389f937e8f6368a46177f8d5833ef3ed8cbf55ca385f`  
		Last Modified: Tue, 03 Feb 2026 03:42:27 GMT  
		Size: 79.6 MB (79570717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88abf7fe679d2a6222f47236a1790c5146c2dc137a51bc3c698a8c53528d612d`  
		Last Modified: Tue, 03 Feb 2026 03:42:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:d43b37fb50921207b5f16dfbf405bd58a754f2298e8310f56d369193643483c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2e497a783275b14ac0b1c4bf313b0fe7d44a773888603ba6c61d6fc0a7572f`

```dockerfile
```

-	Layers:
	-	`sha256:1072577cfbc2108e58d6afbf9bc28017b42040c3702945b17158b13006fc75f5`  
		Last Modified: Tue, 03 Feb 2026 03:42:25 GMT  
		Size: 6.6 MB (6647803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd909d3c95a142358a90fc8722911c17bfd2a904148cff04d32cde335bb03e8`  
		Last Modified: Tue, 03 Feb 2026 03:42:24 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7347d2646b5f45a5b6db7d2b7c55f451e7526f21db079268cb89a21234473a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157136721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4f780e1d08a95afe0c1ccde1f4edab8e9ad4c4d90c5229d2ca280d66e31ce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:42:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:42:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:42:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e726832fe5a5c92dd689aff89da387dfd545c947c6233589660b3f3669420dbe`  
		Last Modified: Tue, 13 Jan 2026 04:42:43 GMT  
		Size: 73.3 MB (73290783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8923ad93aec8a70e3c96191fd9846e9633e80aae6c51dd10c2866dd2e41e3c`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:ca81be3c6b218fa35d12d97a8afdac2e00a14f3ae09836bee37dc03f1604d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f210c3da4b3d7f35eb6937c3e6fd0a0d350a352d3fbfbc68052fb7064af3d37`

```dockerfile
```

-	Layers:
	-	`sha256:aeb9c29c52169ce56a0b4b8a8bd3cf6c5eb6cc5579a30450e14f7711aa008eab`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 6.6 MB (6642400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f487977cbba703ae72c1086a6ed26eed4dad58ec385f7c01cfb323d9c71b19`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8019dc96150cece1b475bde2cad007b9cb3e12bbab126926a41f170104bc1aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162941778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8519b51760b81e62017830c189985cb430b75c1d00d43a3ac48060b898472490`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:59:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 03 Feb 2026 03:59:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:59:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:59:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:59:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:59:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15d2cf910f3f96672825849bca6af844f1d7bbedb700228f0aa02997f38811d`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 18.9 MB (18885881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c86a4abdd2c7ac0e1d11ff7c6fb76ae9125d1408757520619e858201e9ae44`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fd94839986c937b4589e5cd6a1f173610c0faa1425d887cc1121cb890105d2`  
		Last Modified: Tue, 03 Feb 2026 03:59:21 GMT  
		Size: 72.1 MB (72079424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be668b63d2a02dcb0bc1b0c9260cf849be895185eed3022ff7ac2322bdbcb49a`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:c288ba8d56120c571d25fcb9fd1e26dd313d2e929bd1d617e674fe48ae9bb422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6663016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a75943031ce18bca08be0266c5c54c8c48fa76a11d57e2547ee1f312901d6ab`

```dockerfile
```

-	Layers:
	-	`sha256:c01830c10a6b71a969d9f03bba9591dbfee5fda0cdae4265585573c987b18576`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 6.6 MB (6648479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0cf69474343e1ac6e1d3f60af92c90412ed5c5e447764a5fdca734479f3c55`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:1c67d350b4b97e6ef2c52d04c5a2b606038700b27c30be1fcc827c83d0750a90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9d4345e1cbea1692800b2bca89494a285dcdaa455d92ab5477366cf36c9c2e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85738081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3597a88f010efa8c7ae4f264f02c6ad85d626f9a0eefc21ccaf48540739cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:40 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:49:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db80302b016defca3353492ca7c69f65db624dc6d54d024637ba8ba208850ef`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e58ddbb2a68e9d1ec1a1d042347ef3b4855d97c57682045f6270d4d6ce65e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 2.6 MB (2563630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee38868a04a63efb19c32997823ce073d4d9be80d4e550105f70e2ae1bf16aca`  
		Last Modified: Wed, 28 Jan 2026 03:50:06 GMT  
		Size: 79.4 MB (79368676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea97445439cc0d1b2cc6a71d85464903745b6178429c75c2d2d7e0171384e2`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:445328e3ce2e66cb85d892cc6b99f7798d01a4486949a22c5d6d2f2069a7db7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb527adc4e3ce61db447b66ae5adbdb2f7ec85f40b0c52e579cc26e2647fc0d`

```dockerfile
```

-	Layers:
	-	`sha256:d9182e5ff44eee6bc219f9e41785816ff8d2e9fc6e8bebcb6467e56cba51cfb7`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b292c7a96e63a10e77e2dd531cb8e17f1217bf8984cfbfdff44ce7a0d80632`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9bb580f67318869d8c3bbffd0a74ae79e9f956146bc92e373cf53f84e9e8b083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78645343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee82eedad832ef0ab6940d14b7abb701ba0cf8236e54281c11563a70abcf95b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:55:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:55:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:56:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765c2e9488726202408b292c3bac6681d93508efc6e9b2e31e049443567e86e0`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3740b37ea70449e245a9450fc906cc28ba6b7da57b398514750aacfc86b1d6`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 2.6 MB (2627594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1aca9cb457419a7597e00416afd07021750d63f302bb9c4682cfed96fe6e60`  
		Last Modified: Wed, 28 Jan 2026 03:56:17 GMT  
		Size: 71.9 MB (71877331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73362025389d6291b89519a9ae98aaf7933a67f20ce60d58dc6f6fb3c319fd8`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5a1d3b60fe8ea0f375b2edd76de7b0562a301c54a6c16b659996e1309d5e66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75036200048cf02c5b626a83dd60adfc0691bb3e378a6f72fb6611670b0d4fbf`

```dockerfile
```

-	Layers:
	-	`sha256:e9293a685398b5fdd11336f57a7027774d95fcd5ed44adff467f472929367767`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c0437ff9d4a470eaa9b4e3b11c362bdff43f1305a03cc25a83c8655dcbcf9d`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:a30facfc4c52ffe93d7dacff73cda1dc22aa75930f5f8153c0bf6fb7a3068fec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4` - linux; amd64

```console
$ docker pull telegraf@sha256:993f35a9701d19adb4307f93239f5714f58e7960104c4f32d05ae61ca4d45866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171040750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb816d6824a287813e71886bfb01d700431acfada0dbb64d665c11fa57e2de6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:42:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 03 Feb 2026 03:42:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:42:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:42:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:42:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cb6409cdbe5467f35f1e3af1f88ce3933242a9c8b47f40d03df4050a55b92f`  
		Last Modified: Tue, 03 Feb 2026 03:42:25 GMT  
		Size: 18.9 MB (18944427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940ef600ddcf6d55097765a9f871acc42e3e0a63d1db450b877a1278814ebc9a`  
		Last Modified: Tue, 03 Feb 2026 03:42:24 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc279bbe89fbc3b5468389f937e8f6368a46177f8d5833ef3ed8cbf55ca385f`  
		Last Modified: Tue, 03 Feb 2026 03:42:27 GMT  
		Size: 79.6 MB (79570717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88abf7fe679d2a6222f47236a1790c5146c2dc137a51bc3c698a8c53528d612d`  
		Last Modified: Tue, 03 Feb 2026 03:42:24 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:d43b37fb50921207b5f16dfbf405bd58a754f2298e8310f56d369193643483c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2e497a783275b14ac0b1c4bf313b0fe7d44a773888603ba6c61d6fc0a7572f`

```dockerfile
```

-	Layers:
	-	`sha256:1072577cfbc2108e58d6afbf9bc28017b42040c3702945b17158b13006fc75f5`  
		Last Modified: Tue, 03 Feb 2026 03:42:25 GMT  
		Size: 6.6 MB (6647803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd909d3c95a142358a90fc8722911c17bfd2a904148cff04d32cde335bb03e8`  
		Last Modified: Tue, 03 Feb 2026 03:42:24 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7347d2646b5f45a5b6db7d2b7c55f451e7526f21db079268cb89a21234473a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157136721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4f780e1d08a95afe0c1ccde1f4edab8e9ad4c4d90c5229d2ca280d66e31ce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 13 Jan 2026 04:42:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:42:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:42:22 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e726832fe5a5c92dd689aff89da387dfd545c947c6233589660b3f3669420dbe`  
		Last Modified: Tue, 13 Jan 2026 04:42:43 GMT  
		Size: 73.3 MB (73290783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8923ad93aec8a70e3c96191fd9846e9633e80aae6c51dd10c2866dd2e41e3c`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:ca81be3c6b218fa35d12d97a8afdac2e00a14f3ae09836bee37dc03f1604d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f210c3da4b3d7f35eb6937c3e6fd0a0d350a352d3fbfbc68052fb7064af3d37`

```dockerfile
```

-	Layers:
	-	`sha256:aeb9c29c52169ce56a0b4b8a8bd3cf6c5eb6cc5579a30450e14f7711aa008eab`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 6.6 MB (6642400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f487977cbba703ae72c1086a6ed26eed4dad58ec385f7c01cfb323d9c71b19`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8019dc96150cece1b475bde2cad007b9cb3e12bbab126926a41f170104bc1aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162941778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8519b51760b81e62017830c189985cb430b75c1d00d43a3ac48060b898472490`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:59:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 03 Feb 2026 03:59:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:59:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:59:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:59:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:59:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15d2cf910f3f96672825849bca6af844f1d7bbedb700228f0aa02997f38811d`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 18.9 MB (18885881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c86a4abdd2c7ac0e1d11ff7c6fb76ae9125d1408757520619e858201e9ae44`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fd94839986c937b4589e5cd6a1f173610c0faa1425d887cc1121cb890105d2`  
		Last Modified: Tue, 03 Feb 2026 03:59:21 GMT  
		Size: 72.1 MB (72079424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be668b63d2a02dcb0bc1b0c9260cf849be895185eed3022ff7ac2322bdbcb49a`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:c288ba8d56120c571d25fcb9fd1e26dd313d2e929bd1d617e674fe48ae9bb422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6663016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a75943031ce18bca08be0266c5c54c8c48fa76a11d57e2547ee1f312901d6ab`

```dockerfile
```

-	Layers:
	-	`sha256:c01830c10a6b71a969d9f03bba9591dbfee5fda0cdae4265585573c987b18576`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 6.6 MB (6648479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0cf69474343e1ac6e1d3f60af92c90412ed5c5e447764a5fdca734479f3c55`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:1c67d350b4b97e6ef2c52d04c5a2b606038700b27c30be1fcc827c83d0750a90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9d4345e1cbea1692800b2bca89494a285dcdaa455d92ab5477366cf36c9c2e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85738081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3597a88f010efa8c7ae4f264f02c6ad85d626f9a0eefc21ccaf48540739cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:40 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:49:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db80302b016defca3353492ca7c69f65db624dc6d54d024637ba8ba208850ef`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e58ddbb2a68e9d1ec1a1d042347ef3b4855d97c57682045f6270d4d6ce65e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 2.6 MB (2563630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee38868a04a63efb19c32997823ce073d4d9be80d4e550105f70e2ae1bf16aca`  
		Last Modified: Wed, 28 Jan 2026 03:50:06 GMT  
		Size: 79.4 MB (79368676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea97445439cc0d1b2cc6a71d85464903745b6178429c75c2d2d7e0171384e2`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:445328e3ce2e66cb85d892cc6b99f7798d01a4486949a22c5d6d2f2069a7db7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb527adc4e3ce61db447b66ae5adbdb2f7ec85f40b0c52e579cc26e2647fc0d`

```dockerfile
```

-	Layers:
	-	`sha256:d9182e5ff44eee6bc219f9e41785816ff8d2e9fc6e8bebcb6467e56cba51cfb7`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b292c7a96e63a10e77e2dd531cb8e17f1217bf8984cfbfdff44ce7a0d80632`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9bb580f67318869d8c3bbffd0a74ae79e9f956146bc92e373cf53f84e9e8b083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78645343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee82eedad832ef0ab6940d14b7abb701ba0cf8236e54281c11563a70abcf95b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:55:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:55:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENV TELEGRAF_VERSION=1.35.4
# Wed, 28 Jan 2026 03:56:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765c2e9488726202408b292c3bac6681d93508efc6e9b2e31e049443567e86e0`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3740b37ea70449e245a9450fc906cc28ba6b7da57b398514750aacfc86b1d6`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 2.6 MB (2627594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1aca9cb457419a7597e00416afd07021750d63f302bb9c4682cfed96fe6e60`  
		Last Modified: Wed, 28 Jan 2026 03:56:17 GMT  
		Size: 71.9 MB (71877331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73362025389d6291b89519a9ae98aaf7933a67f20ce60d58dc6f6fb3c319fd8`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5a1d3b60fe8ea0f375b2edd76de7b0562a301c54a6c16b659996e1309d5e66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75036200048cf02c5b626a83dd60adfc0691bb3e378a6f72fb6611670b0d4fbf`

```dockerfile
```

-	Layers:
	-	`sha256:e9293a685398b5fdd11336f57a7027774d95fcd5ed44adff467f472929367767`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c0437ff9d4a470eaa9b4e3b11c362bdff43f1305a03cc25a83c8655dcbcf9d`  
		Last Modified: Wed, 28 Jan 2026 03:56:15 GMT  
		Size: 15.0 KB (15028 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:7be0674c1c356518d213d63e15b6b07888ab73049a1cb0687097604ece9b3df7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36` - linux; amd64

```console
$ docker pull telegraf@sha256:58ccb9d8e37bf557f67083ccce3e3ce4957f396aa8b3fe6129a8d502e23495ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171943579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e3f20886692e01f1d99f88027dac10b597cd9145f18488157e18876b5f9523`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:42:15 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 03 Feb 2026 03:42:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:42:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:42:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adebcbe37ee0b28b113ef36280c6455458368ed2af0b6965088578690bc8088c`  
		Last Modified: Tue, 03 Feb 2026 03:42:35 GMT  
		Size: 18.9 MB (18944371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8632a45db105371a11aaaafe063593e38e4c3005c9e8515171ca1903a9652d4c`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118b7f71b555450d49d9d49983a082e0c3aeaf15d90822d92782e888e03ac5b`  
		Last Modified: Tue, 03 Feb 2026 03:42:37 GMT  
		Size: 80.5 MB (80473585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca118e1f2e299a43c4b2a172acf8e7feb3e52e95efc115ff1ee6cf3bd192a84b`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:54a548c35e12e6257790a36be51864458d0060d9bd94a821cfc2599ea0df7eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b0413842c9078e1c4b311b857b5d837dbe66bdefcb8babfef7b0e7b81799f7`

```dockerfile
```

-	Layers:
	-	`sha256:69f944bbe02db18c3ee58b90bd0a508cab1be275ba99898419e87e85789b85b3`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570f9ac06bc5b8da6360ede69f478f33ff6734e1fa1bf429f2ad428f4729a991`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:55191d404c1e659a7991d3fc66fe17db0700db049e9ef527a48abc49c2164852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157809564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee52b4f7d026fcff09727aacc9fbb46d51f03fbf65bde1ac3a7634a65efc39d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:43:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3260264734f11a0dcf2c688e6b709c967bfbe661975d9620e42eedf009712d`  
		Last Modified: Tue, 13 Jan 2026 04:43:30 GMT  
		Size: 74.0 MB (73963627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31439ca9ab7543fb88a1c0663ac62b7650fe5289524a5808103d51482d333336`  
		Last Modified: Tue, 13 Jan 2026 04:43:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:f73fb5631c018efc8c33c79cab881f3bd4e914c16865b14206777b1e3c4e3f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f41fd4ef82359cffad0da19e077e9d1193b1d6d22b2485bf008208f10376774`

```dockerfile
```

-	Layers:
	-	`sha256:97ba1da3e9ec828f3aaf3930e06277f76cd0ccc27fabadf3381c724b461aaf89`  
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a2a55a05b62dc316ccc44feb478292e528f3362b0debb2aaf523d42653b3df`  
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f850b6057827271ad31030df228290c20c18c6658937a9368c6a02b1dc98cf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162662500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36463ebdacc1bbbcfd63521ee5c015b38529e6e40edb73adc416c41beea96b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:59:02 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 03 Feb 2026 03:59:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:59:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:59:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:59:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:59:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b91157227b63d7d9d4c93838b7fa2c845617dbec6090c9eed5111762363969a`  
		Last Modified: Tue, 03 Feb 2026 03:59:20 GMT  
		Size: 18.9 MB (18885676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4d724e8f80b983796e4ef7f90ae831d54609fdda2318aa4bda4e50cf42a40c`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a540608931d71fb1ec1cb4328da76b883bbc0671e8b853f620324664dda441`  
		Last Modified: Tue, 03 Feb 2026 03:59:21 GMT  
		Size: 71.8 MB (71800349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5431abdf12088b41b867e5d00c1c75f73766831eb10315d27e60e085e1dd9d6`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c497576492db818b40edcd98bffd5b1eeb0d2465209ecfe2ad1f13667b22e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8412438b7acec9586e1a47de053fa93ee0ad9c675be8c55c5d0ffd23d74f563`

```dockerfile
```

-	Layers:
	-	`sha256:ecfe99d582dc5331bc9135bd5200e7a7d87b218ba294917c8df16d2702e1f43e`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb73c2fb327a00dcc6d526a81592b58aa1d3b7083baaa949c2d940be2f3aa9d5`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:7be0674c1c356518d213d63e15b6b07888ab73049a1cb0687097604ece9b3df7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4` - linux; amd64

```console
$ docker pull telegraf@sha256:58ccb9d8e37bf557f67083ccce3e3ce4957f396aa8b3fe6129a8d502e23495ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171943579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e3f20886692e01f1d99f88027dac10b597cd9145f18488157e18876b5f9523`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:42:15 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 03 Feb 2026 03:42:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:42:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:42:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adebcbe37ee0b28b113ef36280c6455458368ed2af0b6965088578690bc8088c`  
		Last Modified: Tue, 03 Feb 2026 03:42:35 GMT  
		Size: 18.9 MB (18944371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8632a45db105371a11aaaafe063593e38e4c3005c9e8515171ca1903a9652d4c`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118b7f71b555450d49d9d49983a082e0c3aeaf15d90822d92782e888e03ac5b`  
		Last Modified: Tue, 03 Feb 2026 03:42:37 GMT  
		Size: 80.5 MB (80473585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca118e1f2e299a43c4b2a172acf8e7feb3e52e95efc115ff1ee6cf3bd192a84b`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:54a548c35e12e6257790a36be51864458d0060d9bd94a821cfc2599ea0df7eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b0413842c9078e1c4b311b857b5d837dbe66bdefcb8babfef7b0e7b81799f7`

```dockerfile
```

-	Layers:
	-	`sha256:69f944bbe02db18c3ee58b90bd0a508cab1be275ba99898419e87e85789b85b3`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570f9ac06bc5b8da6360ede69f478f33ff6734e1fa1bf429f2ad428f4729a991`  
		Last Modified: Tue, 03 Feb 2026 03:42:34 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:55191d404c1e659a7991d3fc66fe17db0700db049e9ef527a48abc49c2164852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157809564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee52b4f7d026fcff09727aacc9fbb46d51f03fbf65bde1ac3a7634a65efc39d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:42:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 13 Jan 2026 04:43:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d545d030870d426bc777e5c833ddeec574860b248b830258001d7e907fbfb5f`  
		Last Modified: Tue, 13 Jan 2026 04:42:41 GMT  
		Size: 17.7 MB (17699906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74a543c626b9ad2235b7e89bb12796cca45fa6bb0e5917c371a42b8d5025ca`  
		Last Modified: Tue, 13 Jan 2026 04:42:40 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3260264734f11a0dcf2c688e6b709c967bfbe661975d9620e42eedf009712d`  
		Last Modified: Tue, 13 Jan 2026 04:43:30 GMT  
		Size: 74.0 MB (73963627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31439ca9ab7543fb88a1c0663ac62b7650fe5289524a5808103d51482d333336`  
		Last Modified: Tue, 13 Jan 2026 04:43:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:f73fb5631c018efc8c33c79cab881f3bd4e914c16865b14206777b1e3c4e3f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f41fd4ef82359cffad0da19e077e9d1193b1d6d22b2485bf008208f10376774`

```dockerfile
```

-	Layers:
	-	`sha256:97ba1da3e9ec828f3aaf3930e06277f76cd0ccc27fabadf3381c724b461aaf89`  
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a2a55a05b62dc316ccc44feb478292e528f3362b0debb2aaf523d42653b3df`  
		Last Modified: Tue, 13 Jan 2026 04:43:28 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f850b6057827271ad31030df228290c20c18c6658937a9368c6a02b1dc98cf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162662500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36463ebdacc1bbbcfd63521ee5c015b38529e6e40edb73adc416c41beea96b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:58:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:59:02 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 03 Feb 2026 03:59:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:59:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:59:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:59:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:59:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b91157227b63d7d9d4c93838b7fa2c845617dbec6090c9eed5111762363969a`  
		Last Modified: Tue, 03 Feb 2026 03:59:20 GMT  
		Size: 18.9 MB (18885676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4d724e8f80b983796e4ef7f90ae831d54609fdda2318aa4bda4e50cf42a40c`  
		Last Modified: Tue, 03 Feb 2026 03:59:18 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a540608931d71fb1ec1cb4328da76b883bbc0671e8b853f620324664dda441`  
		Last Modified: Tue, 03 Feb 2026 03:59:21 GMT  
		Size: 71.8 MB (71800349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5431abdf12088b41b867e5d00c1c75f73766831eb10315d27e60e085e1dd9d6`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:3c497576492db818b40edcd98bffd5b1eeb0d2465209ecfe2ad1f13667b22e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8412438b7acec9586e1a47de053fa93ee0ad9c675be8c55c5d0ffd23d74f563`

```dockerfile
```

-	Layers:
	-	`sha256:ecfe99d582dc5331bc9135bd5200e7a7d87b218ba294917c8df16d2702e1f43e`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb73c2fb327a00dcc6d526a81592b58aa1d3b7083baaa949c2d940be2f3aa9d5`  
		Last Modified: Tue, 03 Feb 2026 03:59:19 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:d9c658cf29f505b91bd830f60720c5cc6a9e2e131198d6e2b6e525d58ecfa2d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37` - linux; amd64

```console
$ docker pull telegraf@sha256:fce59f7435a59b96a2e2253232287155c705300dc44cd0b0e4893b4eb6d650ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171888870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb378fa5700638e46dd40a6997ef7329656114e812994435a4439aaedcb36e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 03 Feb 2026 03:42:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:42:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a21b6c21a270e5360e264c6c2346a83ebc0264f129b6ec772afbf07428f8ad7`  
		Last Modified: Tue, 03 Feb 2026 03:42:44 GMT  
		Size: 18.9 MB (18944513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922cb3d58ddf8f8fb619712d8178640e096db5c385d777ab9ec364c37ba189f`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc606ff27378ce27814dc9fb68eb33b1ed090997f036bf0356e6b69d095dde`  
		Last Modified: Tue, 03 Feb 2026 03:42:46 GMT  
		Size: 80.4 MB (80418733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427588db874e513d7225d1a28c889a0009eb8bf4a286d22a78ee62ce14a1d372`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:fae71791835010f5ee54aadb7345baa99da67e360a624b7d9c0ff3e4c346040d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f093d6308a45ea4b48d6dd875342c76dc8d4a8f2ed95b55beaa4967b175d8c5`

```dockerfile
```

-	Layers:
	-	`sha256:214ee1200286d9f64dc1055a7f616c69285769a03c70e99749824a30d7ea4a0b`  
		Last Modified: Tue, 03 Feb 2026 03:42:44 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f6f5646450619ed6c17dda96217faab5481e2c1cb7f4f83fa1843571f8b1c4`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf62ac35ce9687face50fd2639feb43a822a1aadc56849ea6c60b22501a6b414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e3b71af3c7c76e337b1db47ed652ce2d1be21c262c65e89ecf32cac729f3e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:43:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9de7ad08dcb55771b6ddde8b11f6be1cab673bc19b2c17a508afcf0e038fe`  
		Last Modified: Tue, 13 Jan 2026 04:43:37 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2b991059e5fc2e044e861b3c4b17e51e5060c3b3866144670a8ba2808738eb`  
		Last Modified: Tue, 13 Jan 2026 04:43:38 GMT  
		Size: 74.3 MB (74283228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70bfa42881d9120c2c8521d7af4537f02fbf0603426a3e0b88be6c6a773248f`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:12ddfd8a917b929e25e6d5a67b84236c387e7395f1e2224cc9df15ee37e517c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29413c178f6b4e8dbe33aef6c179252b1cc41587b29c8bf31fe73c50dab95f25`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9dff5bd5b655aec0dd0a533e719c6d1a8fc2f0ba622b7c710730c0acf45c1`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ccf5f17de150fe1deb37fa8e3acf538d610014d40ad30c61eb7e7d199520360d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162699202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fb9d4745af3e9e4b6ef1d814d8f4e4ef3457135f9b2db861f37f34b6a7eea6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:59:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:59:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 03 Feb 2026 03:59:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:59:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:59:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b82a31d187efe91e536fa58d384b6b5e8375ca6a7bfa79153bc24dc42c230`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 18.9 MB (18885953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5d273d4a887815c216f2ccf896f402ed24a7ba89780fa04aac5a6b0e09224c`  
		Last Modified: Tue, 03 Feb 2026 03:59:39 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46ef1e6fac97cee7cf9d784730bb0bd2be38ef3629f0a4cbe9ca906bab0fb82`  
		Last Modified: Tue, 03 Feb 2026 03:59:42 GMT  
		Size: 71.8 MB (71836772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612422b8ed014b833c9ff5e67f7a2b8b6cc5b8a0c793803f34b0b3c1162e8bb0`  
		Last Modified: Tue, 03 Feb 2026 03:59:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:eb3c6bcd11ddc38d64eeb1b250c96fa30fd64eb71b758015dc6416771c11c305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454ed185d31db87b5ee6d10bd2485c3f44d732088547abeb74734f54e7c981ca`

```dockerfile
```

-	Layers:
	-	`sha256:4f73bfe70606c0be69eda657064d490413afcee71f3bb90a48ce854ccd0c5ced`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86569a8a7946486d2606863907791e441d76077ff8c3f879e663fcf162b93291`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:98d238fac269c949f0574ed7a1fec403b1acf79be4f0c4ec38941f94de1d566a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f532da2eb8b819a3a270f9c751e89331da81c86940bfd27281f8b85eb85eaff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86581620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b2b5dd6c4243f44d050b74b97814e4de1cb50fd8b9ebd1b8f1b291e5c179de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:49:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8ea768bc4c5628c8e56d287d7a67720c9b15bde9850b70d0a05723f51936`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ad1e390f36b724abd91aa22a28eb46c025163a62dc0911807357e78154a8e`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 80.2 MB (80212230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9551f385152eb62f889eeac14aa6f4c2a25647891cda4c7c90f2ca653dd93ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1e3ddddbda26a225a059e6e2a379518112e670d949e6f7abecba16226be11b`

```dockerfile
```

-	Layers:
	-	`sha256:881320f646701d701accef70533b21fd01b1228efa3f5a08799dac74e5fb5bc4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f4f5b027d0939ab896d19fef833e0975aa6b329dc393c086859740b7cdc765`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ddc91fe454b27a2b140a694c51938b3634275cf386cb9bb5a06a3c814fe4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78398298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e03eca0c8ec323879f457dc6137397bd850cccee5c292654e3601eae5febacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:12 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ea420ed678b641ffe5a2375797d77f159e1c6d7d7bc21dd50e5ba6c40e4e4`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979f17c250ed04c44e760bb1df516f6382cc558c1de3b324a98ab37d99229ee`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 2.6 MB (2627628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d72b6efebcdd0e2dd86e573eabc9bb26ef060fd1601036f495294ede9ae77`  
		Last Modified: Wed, 28 Jan 2026 03:56:33 GMT  
		Size: 71.6 MB (71630252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684706cc32aedd8438e6eeab7b7b636b198f3f53cc99cf7357028c3b3a7ca505`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8e4fdf60c586a5bd4b42c2a03ebc59c0f42921f887cf6b64620d69d21a3ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720d80d3926d8e1a966a4f920c28b6479880e8acdabe11d3c83c7a4382220f9`

```dockerfile
```

-	Layers:
	-	`sha256:3ed6e0a713bc070c69819eda05cc98e39c8ff92c5aa86971557bed38cbc3901a`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726dbaed541995327adbca51afdd5d39292bfeeb2b73c30ee45a231287dcd04d`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 15.3 KB (15341 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.1`

```console
$ docker pull telegraf@sha256:d9c658cf29f505b91bd830f60720c5cc6a9e2e131198d6e2b6e525d58ecfa2d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.1` - linux; amd64

```console
$ docker pull telegraf@sha256:fce59f7435a59b96a2e2253232287155c705300dc44cd0b0e4893b4eb6d650ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171888870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb378fa5700638e46dd40a6997ef7329656114e812994435a4439aaedcb36e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 03 Feb 2026 03:42:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:42:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a21b6c21a270e5360e264c6c2346a83ebc0264f129b6ec772afbf07428f8ad7`  
		Last Modified: Tue, 03 Feb 2026 03:42:44 GMT  
		Size: 18.9 MB (18944513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922cb3d58ddf8f8fb619712d8178640e096db5c385d777ab9ec364c37ba189f`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc606ff27378ce27814dc9fb68eb33b1ed090997f036bf0356e6b69d095dde`  
		Last Modified: Tue, 03 Feb 2026 03:42:46 GMT  
		Size: 80.4 MB (80418733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427588db874e513d7225d1a28c889a0009eb8bf4a286d22a78ee62ce14a1d372`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:fae71791835010f5ee54aadb7345baa99da67e360a624b7d9c0ff3e4c346040d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f093d6308a45ea4b48d6dd875342c76dc8d4a8f2ed95b55beaa4967b175d8c5`

```dockerfile
```

-	Layers:
	-	`sha256:214ee1200286d9f64dc1055a7f616c69285769a03c70e99749824a30d7ea4a0b`  
		Last Modified: Tue, 03 Feb 2026 03:42:44 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f6f5646450619ed6c17dda96217faab5481e2c1cb7f4f83fa1843571f8b1c4`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf62ac35ce9687face50fd2639feb43a822a1aadc56849ea6c60b22501a6b414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e3b71af3c7c76e337b1db47ed652ce2d1be21c262c65e89ecf32cac729f3e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:43:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9de7ad08dcb55771b6ddde8b11f6be1cab673bc19b2c17a508afcf0e038fe`  
		Last Modified: Tue, 13 Jan 2026 04:43:37 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2b991059e5fc2e044e861b3c4b17e51e5060c3b3866144670a8ba2808738eb`  
		Last Modified: Tue, 13 Jan 2026 04:43:38 GMT  
		Size: 74.3 MB (74283228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70bfa42881d9120c2c8521d7af4537f02fbf0603426a3e0b88be6c6a773248f`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:12ddfd8a917b929e25e6d5a67b84236c387e7395f1e2224cc9df15ee37e517c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29413c178f6b4e8dbe33aef6c179252b1cc41587b29c8bf31fe73c50dab95f25`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9dff5bd5b655aec0dd0a533e719c6d1a8fc2f0ba622b7c710730c0acf45c1`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ccf5f17de150fe1deb37fa8e3acf538d610014d40ad30c61eb7e7d199520360d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162699202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fb9d4745af3e9e4b6ef1d814d8f4e4ef3457135f9b2db861f37f34b6a7eea6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:59:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:59:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 03 Feb 2026 03:59:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:59:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:59:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b82a31d187efe91e536fa58d384b6b5e8375ca6a7bfa79153bc24dc42c230`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 18.9 MB (18885953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5d273d4a887815c216f2ccf896f402ed24a7ba89780fa04aac5a6b0e09224c`  
		Last Modified: Tue, 03 Feb 2026 03:59:39 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46ef1e6fac97cee7cf9d784730bb0bd2be38ef3629f0a4cbe9ca906bab0fb82`  
		Last Modified: Tue, 03 Feb 2026 03:59:42 GMT  
		Size: 71.8 MB (71836772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612422b8ed014b833c9ff5e67f7a2b8b6cc5b8a0c793803f34b0b3c1162e8bb0`  
		Last Modified: Tue, 03 Feb 2026 03:59:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:eb3c6bcd11ddc38d64eeb1b250c96fa30fd64eb71b758015dc6416771c11c305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454ed185d31db87b5ee6d10bd2485c3f44d732088547abeb74734f54e7c981ca`

```dockerfile
```

-	Layers:
	-	`sha256:4f73bfe70606c0be69eda657064d490413afcee71f3bb90a48ce854ccd0c5ced`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86569a8a7946486d2606863907791e441d76077ff8c3f879e663fcf162b93291`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.1-alpine`

```console
$ docker pull telegraf@sha256:98d238fac269c949f0574ed7a1fec403b1acf79be4f0c4ec38941f94de1d566a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f532da2eb8b819a3a270f9c751e89331da81c86940bfd27281f8b85eb85eaff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86581620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b2b5dd6c4243f44d050b74b97814e4de1cb50fd8b9ebd1b8f1b291e5c179de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:49:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8ea768bc4c5628c8e56d287d7a67720c9b15bde9850b70d0a05723f51936`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ad1e390f36b724abd91aa22a28eb46c025163a62dc0911807357e78154a8e`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 80.2 MB (80212230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9551f385152eb62f889eeac14aa6f4c2a25647891cda4c7c90f2ca653dd93ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1e3ddddbda26a225a059e6e2a379518112e670d949e6f7abecba16226be11b`

```dockerfile
```

-	Layers:
	-	`sha256:881320f646701d701accef70533b21fd01b1228efa3f5a08799dac74e5fb5bc4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f4f5b027d0939ab896d19fef833e0975aa6b329dc393c086859740b7cdc765`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ddc91fe454b27a2b140a694c51938b3634275cf386cb9bb5a06a3c814fe4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78398298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e03eca0c8ec323879f457dc6137397bd850cccee5c292654e3601eae5febacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:12 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ea420ed678b641ffe5a2375797d77f159e1c6d7d7bc21dd50e5ba6c40e4e4`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979f17c250ed04c44e760bb1df516f6382cc558c1de3b324a98ab37d99229ee`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 2.6 MB (2627628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d72b6efebcdd0e2dd86e573eabc9bb26ef060fd1601036f495294ede9ae77`  
		Last Modified: Wed, 28 Jan 2026 03:56:33 GMT  
		Size: 71.6 MB (71630252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684706cc32aedd8438e6eeab7b7b636b198f3f53cc99cf7357028c3b3a7ca505`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8e4fdf60c586a5bd4b42c2a03ebc59c0f42921f887cf6b64620d69d21a3ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720d80d3926d8e1a966a4f920c28b6479880e8acdabe11d3c83c7a4382220f9`

```dockerfile
```

-	Layers:
	-	`sha256:3ed6e0a713bc070c69819eda05cc98e39c8ff92c5aa86971557bed38cbc3901a`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726dbaed541995327adbca51afdd5d39292bfeeb2b73c30ee45a231287dcd04d`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 15.3 KB (15341 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:98d238fac269c949f0574ed7a1fec403b1acf79be4f0c4ec38941f94de1d566a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f532da2eb8b819a3a270f9c751e89331da81c86940bfd27281f8b85eb85eaff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86581620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b2b5dd6c4243f44d050b74b97814e4de1cb50fd8b9ebd1b8f1b291e5c179de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:49:45 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8ea768bc4c5628c8e56d287d7a67720c9b15bde9850b70d0a05723f51936`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ad1e390f36b724abd91aa22a28eb46c025163a62dc0911807357e78154a8e`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 80.2 MB (80212230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9551f385152eb62f889eeac14aa6f4c2a25647891cda4c7c90f2ca653dd93ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1e3ddddbda26a225a059e6e2a379518112e670d949e6f7abecba16226be11b`

```dockerfile
```

-	Layers:
	-	`sha256:881320f646701d701accef70533b21fd01b1228efa3f5a08799dac74e5fb5bc4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f4f5b027d0939ab896d19fef833e0975aa6b329dc393c086859740b7cdc765`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ddc91fe454b27a2b140a694c51938b3634275cf386cb9bb5a06a3c814fe4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78398298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e03eca0c8ec323879f457dc6137397bd850cccee5c292654e3601eae5febacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:12 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
ENV TELEGRAF_VERSION=1.37.1
# Wed, 28 Jan 2026 03:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:17 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ea420ed678b641ffe5a2375797d77f159e1c6d7d7bc21dd50e5ba6c40e4e4`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979f17c250ed04c44e760bb1df516f6382cc558c1de3b324a98ab37d99229ee`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 2.6 MB (2627628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d72b6efebcdd0e2dd86e573eabc9bb26ef060fd1601036f495294ede9ae77`  
		Last Modified: Wed, 28 Jan 2026 03:56:33 GMT  
		Size: 71.6 MB (71630252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684706cc32aedd8438e6eeab7b7b636b198f3f53cc99cf7357028c3b3a7ca505`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c8e4fdf60c586a5bd4b42c2a03ebc59c0f42921f887cf6b64620d69d21a3ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720d80d3926d8e1a966a4f920c28b6479880e8acdabe11d3c83c7a4382220f9`

```dockerfile
```

-	Layers:
	-	`sha256:3ed6e0a713bc070c69819eda05cc98e39c8ff92c5aa86971557bed38cbc3901a`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726dbaed541995327adbca51afdd5d39292bfeeb2b73c30ee45a231287dcd04d`  
		Last Modified: Wed, 28 Jan 2026 03:56:31 GMT  
		Size: 15.3 KB (15341 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:d9c658cf29f505b91bd830f60720c5cc6a9e2e131198d6e2b6e525d58ecfa2d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:fce59f7435a59b96a2e2253232287155c705300dc44cd0b0e4893b4eb6d650ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171888870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb378fa5700638e46dd40a6997ef7329656114e812994435a4439aaedcb36e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:42:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 03 Feb 2026 03:42:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:42:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:42:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:42:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a21b6c21a270e5360e264c6c2346a83ebc0264f129b6ec772afbf07428f8ad7`  
		Last Modified: Tue, 03 Feb 2026 03:42:44 GMT  
		Size: 18.9 MB (18944513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5922cb3d58ddf8f8fb619712d8178640e096db5c385d777ab9ec364c37ba189f`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc606ff27378ce27814dc9fb68eb33b1ed090997f036bf0356e6b69d095dde`  
		Last Modified: Tue, 03 Feb 2026 03:42:46 GMT  
		Size: 80.4 MB (80418733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427588db874e513d7225d1a28c889a0009eb8bf4a286d22a78ee62ce14a1d372`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:fae71791835010f5ee54aadb7345baa99da67e360a624b7d9c0ff3e4c346040d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f093d6308a45ea4b48d6dd875342c76dc8d4a8f2ed95b55beaa4967b175d8c5`

```dockerfile
```

-	Layers:
	-	`sha256:214ee1200286d9f64dc1055a7f616c69285769a03c70e99749824a30d7ea4a0b`  
		Last Modified: Tue, 03 Feb 2026 03:42:44 GMT  
		Size: 6.7 MB (6667266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f6f5646450619ed6c17dda96217faab5481e2c1cb7f4f83fa1843571f8b1c4`  
		Last Modified: Tue, 03 Feb 2026 03:42:43 GMT  
		Size: 14.7 KB (14728 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cf62ac35ce9687face50fd2639feb43a822a1aadc56849ea6c60b22501a6b414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158129223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e3b71af3c7c76e337b1db47ed652ce2d1be21c262c65e89ecf32cac729f3e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:43:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 13 Jan 2026 04:43:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 13 Jan 2026 04:43:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:43:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9de7ad08dcb55771b6ddde8b11f6be1cab673bc19b2c17a508afcf0e038fe`  
		Last Modified: Tue, 13 Jan 2026 04:43:37 GMT  
		Size: 17.7 MB (17699967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdd328b63edbfc32eae2bdc1cc9e3b04b04526a41ff244097abe4ae2ccf35e2`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2b991059e5fc2e044e861b3c4b17e51e5060c3b3866144670a8ba2808738eb`  
		Last Modified: Tue, 13 Jan 2026 04:43:38 GMT  
		Size: 74.3 MB (74283228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70bfa42881d9120c2c8521d7af4537f02fbf0603426a3e0b88be6c6a773248f`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:12ddfd8a917b929e25e6d5a67b84236c387e7395f1e2224cc9df15ee37e517c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29413c178f6b4e8dbe33aef6c179252b1cc41587b29c8bf31fe73c50dab95f25`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9dff5bd5b655aec0dd0a533e719c6d1a8fc2f0ba622b7c710730c0acf45c1`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 6.7 MB (6661871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa7f8059928d92ad74587569e803f4e0bd49de8de136b0abf82bd8ea2d59a25`  
		Last Modified: Tue, 13 Jan 2026 04:43:36 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ccf5f17de150fe1deb37fa8e3acf538d610014d40ad30c61eb7e7d199520360d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162699202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fb9d4745af3e9e4b6ef1d814d8f4e4ef3457135f9b2db861f37f34b6a7eea6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:59:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:59:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
ENV TELEGRAF_VERSION=1.37.1
# Tue, 03 Feb 2026 03:59:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 03 Feb 2026 03:59:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 03 Feb 2026 03:59:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:59:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b82a31d187efe91e536fa58d384b6b5e8375ca6a7bfa79153bc24dc42c230`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 18.9 MB (18885953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5d273d4a887815c216f2ccf896f402ed24a7ba89780fa04aac5a6b0e09224c`  
		Last Modified: Tue, 03 Feb 2026 03:59:39 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46ef1e6fac97cee7cf9d784730bb0bd2be38ef3629f0a4cbe9ca906bab0fb82`  
		Last Modified: Tue, 03 Feb 2026 03:59:42 GMT  
		Size: 71.8 MB (71836772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612422b8ed014b833c9ff5e67f7a2b8b6cc5b8a0c793803f34b0b3c1162e8bb0`  
		Last Modified: Tue, 03 Feb 2026 03:59:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:eb3c6bcd11ddc38d64eeb1b250c96fa30fd64eb71b758015dc6416771c11c305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454ed185d31db87b5ee6d10bd2485c3f44d732088547abeb74734f54e7c981ca`

```dockerfile
```

-	Layers:
	-	`sha256:4f73bfe70606c0be69eda657064d490413afcee71f3bb90a48ce854ccd0c5ced`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 6.7 MB (6667954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86569a8a7946486d2606863907791e441d76077ff8c3f879e663fcf162b93291`  
		Last Modified: Tue, 03 Feb 2026 03:59:40 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
