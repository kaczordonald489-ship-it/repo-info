<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.8`](#chronograf1108)
-	[`chronograf:1.10.8-alpine`](#chronograf1108-alpine)
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
$ docker pull chronograf@sha256:1140faa8c1bb598f1660c359a5db8fc40bd9f325109f5983156a835725548890
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
$ docker pull chronograf@sha256:9e7f5b612bbdb4be8675320e3ff7d3bf1c942ad06970c3f170d2c1dd329792a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ced03eba5efa1482e1606ca10c179fccef17967909c68b4e339a4d855a5c5fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:11:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 05:12:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:12:01 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:12:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff136bf2c7928ce0501ad7b858da691f60acd2ce2dd42c72ed7d0e879ece89ed`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 7.9 MB (7878770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22554aeaa4ff175a76313f43728ecc9641a4ff235f2f4426cb058478def98ba`  
		Last Modified: Tue, 18 Nov 2025 05:12:24 GMT  
		Size: 49.3 MB (49276640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7443cf8f1612d0ed8cf6c8e4d3b107b6514849725b1f82366c4cd453226aef6`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b57c07510327eb66bc1223c4af94766640a29095f6a5d17a91fa16e2148a21`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0413830ddd1599611bcaf02d2d9a43a716bb81c68202fe9e3b8f9c6b0905031`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:165854fe1b463d83716d5698cffb26dc4dcdd9c1b99715c1dfed3535e5d92161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eae45dafd7ac73a76acf5ee362fe669a44a19aefc82736a176ded2fc045e4d`

```dockerfile
```

-	Layers:
	-	`sha256:3f3163a68ece5bd266953666fbfba8eddcd716dad3ce4dce620aaaf9cb60a224`  
		Last Modified: Tue, 18 Nov 2025 07:39:53 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5c611aa284b2ca4de5bb9c5a715eefbdb161a1b37f0aedcde60010234e4c4e`  
		Last Modified: Tue, 18 Nov 2025 07:39:54 GMT  
		Size: 16.1 KB (16083 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e1b13de5c8ec347837c2f5d250d1c2e80865aa445517aa06fc0bcc9e25b14abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25913dc7e88da6be5c53fe3140175f460a68f14f55856a3ebd12f5225ff6e164`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:17:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 04:17:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:17:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:17:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:17:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090570ce97227c589c84da564663c17964737bd94f351c5e4277316e34e3328b`  
		Last Modified: Tue, 18 Nov 2025 04:18:01 GMT  
		Size: 6.5 MB (6508158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe50b4d4c0e57c5aa2a1dafec359d48e73679be75d7397877754b72352c37d`  
		Last Modified: Tue, 18 Nov 2025 04:18:05 GMT  
		Size: 45.6 MB (45621855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c4be73ab28d36ccf2884b0f3b83104d0e8dee5b3601ff29c331c7a60ab522e`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a747e3b835cd3b4d70b4186e5553c8e17eb6b9fa414e0833a90a611809ade433`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4e072645cfa57704d9316047e0e0f4b5bea997852a9ed21594f25497c92cdc`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:361e9a4e047048a444b66447bfc51ba18f4c997afa2098efd5f25584dd9ce6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720f507f08dca7cec9e10d8583e5ce39ffbee7cc1c5dcbb4c329ead1fa4457f1`

```dockerfile
```

-	Layers:
	-	`sha256:9731727bb4381d708af2f7544d7b7836f3a927ce6c31ed95e9c1542540aaf92c`  
		Last Modified: Tue, 18 Nov 2025 07:39:58 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d19a029240d6c9332e0318e801bb38c8157adae3b13448011f5277a5a78e2c`  
		Last Modified: Tue, 18 Nov 2025 07:39:59 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a779993306306e7db8b00934aaaae92e9edf407acf80aabe06b317ceee4a01e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df5325d525c2e46319bb640633ccfaf396d50b3d2938ddd6c7194707a33d287`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:31:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 03:31:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:31:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:31:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:31:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0bc461d630893e7099423ad226893ab78dccbc7781b48cbf37e69cd79cd304`  
		Last Modified: Tue, 18 Nov 2025 03:32:19 GMT  
		Size: 7.7 MB (7691863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452cc9063d26f4676d73fa558b77cae141b38c2086158fba9cf70589d9c5e8c7`  
		Last Modified: Tue, 18 Nov 2025 03:32:26 GMT  
		Size: 47.1 MB (47066829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9a3e84192a601f3bd6d3e7ca86dfc08f8933f9ce86856aedd10f2bea4af6e8`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254bd12639bf9c90cc2cf8e22a186d95b868302652ed7b973f245791b4c945fd`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf36cb51c0dfd2bad204ce8824e65b8398e5ab5c176d88df6e621189c859214`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:e7abf137713efc087412f366d56960a46c0ca78af03effaac752a900e34c506b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513d0ddddd8249f753232ffa801c47b1c5d8ce010f554e82c1ea03548467e3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5a44553c7ec7fe634d38a56ac68516bb68ccf2e228ec5cd99a6f6cadc695005e`  
		Last Modified: Tue, 18 Nov 2025 04:41:58 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7f4fe13eead8b0eacedc2971a58c309483750311e140db705345e06a33e877`  
		Last Modified: Tue, 18 Nov 2025 04:41:58 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8`

```console
$ docker pull chronograf@sha256:1140faa8c1bb598f1660c359a5db8fc40bd9f325109f5983156a835725548890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.8` - linux; amd64

```console
$ docker pull chronograf@sha256:9e7f5b612bbdb4be8675320e3ff7d3bf1c942ad06970c3f170d2c1dd329792a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ced03eba5efa1482e1606ca10c179fccef17967909c68b4e339a4d855a5c5fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:11:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 05:12:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:12:01 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:12:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff136bf2c7928ce0501ad7b858da691f60acd2ce2dd42c72ed7d0e879ece89ed`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 7.9 MB (7878770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22554aeaa4ff175a76313f43728ecc9641a4ff235f2f4426cb058478def98ba`  
		Last Modified: Tue, 18 Nov 2025 05:12:24 GMT  
		Size: 49.3 MB (49276640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7443cf8f1612d0ed8cf6c8e4d3b107b6514849725b1f82366c4cd453226aef6`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b57c07510327eb66bc1223c4af94766640a29095f6a5d17a91fa16e2148a21`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0413830ddd1599611bcaf02d2d9a43a716bb81c68202fe9e3b8f9c6b0905031`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:165854fe1b463d83716d5698cffb26dc4dcdd9c1b99715c1dfed3535e5d92161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eae45dafd7ac73a76acf5ee362fe669a44a19aefc82736a176ded2fc045e4d`

```dockerfile
```

-	Layers:
	-	`sha256:3f3163a68ece5bd266953666fbfba8eddcd716dad3ce4dce620aaaf9cb60a224`  
		Last Modified: Tue, 18 Nov 2025 07:39:53 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5c611aa284b2ca4de5bb9c5a715eefbdb161a1b37f0aedcde60010234e4c4e`  
		Last Modified: Tue, 18 Nov 2025 07:39:54 GMT  
		Size: 16.1 KB (16083 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e1b13de5c8ec347837c2f5d250d1c2e80865aa445517aa06fc0bcc9e25b14abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25913dc7e88da6be5c53fe3140175f460a68f14f55856a3ebd12f5225ff6e164`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:17:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 04:17:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:17:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:17:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:17:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090570ce97227c589c84da564663c17964737bd94f351c5e4277316e34e3328b`  
		Last Modified: Tue, 18 Nov 2025 04:18:01 GMT  
		Size: 6.5 MB (6508158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe50b4d4c0e57c5aa2a1dafec359d48e73679be75d7397877754b72352c37d`  
		Last Modified: Tue, 18 Nov 2025 04:18:05 GMT  
		Size: 45.6 MB (45621855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c4be73ab28d36ccf2884b0f3b83104d0e8dee5b3601ff29c331c7a60ab522e`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a747e3b835cd3b4d70b4186e5553c8e17eb6b9fa414e0833a90a611809ade433`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4e072645cfa57704d9316047e0e0f4b5bea997852a9ed21594f25497c92cdc`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:361e9a4e047048a444b66447bfc51ba18f4c997afa2098efd5f25584dd9ce6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720f507f08dca7cec9e10d8583e5ce39ffbee7cc1c5dcbb4c329ead1fa4457f1`

```dockerfile
```

-	Layers:
	-	`sha256:9731727bb4381d708af2f7544d7b7836f3a927ce6c31ed95e9c1542540aaf92c`  
		Last Modified: Tue, 18 Nov 2025 07:39:58 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d19a029240d6c9332e0318e801bb38c8157adae3b13448011f5277a5a78e2c`  
		Last Modified: Tue, 18 Nov 2025 07:39:59 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a779993306306e7db8b00934aaaae92e9edf407acf80aabe06b317ceee4a01e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df5325d525c2e46319bb640633ccfaf396d50b3d2938ddd6c7194707a33d287`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:31:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 03:31:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:31:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:31:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:31:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0bc461d630893e7099423ad226893ab78dccbc7781b48cbf37e69cd79cd304`  
		Last Modified: Tue, 18 Nov 2025 03:32:19 GMT  
		Size: 7.7 MB (7691863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452cc9063d26f4676d73fa558b77cae141b38c2086158fba9cf70589d9c5e8c7`  
		Last Modified: Tue, 18 Nov 2025 03:32:26 GMT  
		Size: 47.1 MB (47066829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9a3e84192a601f3bd6d3e7ca86dfc08f8933f9ce86856aedd10f2bea4af6e8`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254bd12639bf9c90cc2cf8e22a186d95b868302652ed7b973f245791b4c945fd`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf36cb51c0dfd2bad204ce8824e65b8398e5ab5c176d88df6e621189c859214`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:e7abf137713efc087412f366d56960a46c0ca78af03effaac752a900e34c506b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513d0ddddd8249f753232ffa801c47b1c5d8ce010f554e82c1ea03548467e3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5a44553c7ec7fe634d38a56ac68516bb68ccf2e228ec5cd99a6f6cadc695005e`  
		Last Modified: Tue, 18 Nov 2025 04:41:58 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7f4fe13eead8b0eacedc2971a58c309483750311e140db705345e06a33e877`  
		Last Modified: Tue, 18 Nov 2025 04:41:58 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:78c1c40d2c71f8bfd127862e5b96a1a366d39d081a4679107bb2bbc6e9ce7eb1
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
$ docker pull chronograf@sha256:c32bb8ad1ea434871eb8ef30f4939a85b8a4a466f68c9d84f861ef015f1c793c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda210c5adc84b59574a05f318b600b3fc41031bec0ab76e78834ec72866a918`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:11:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 18 Nov 2025 05:11:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:11:09 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:11:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:11:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903b4b7ce27b9621d75e24e8defd50b933d8b556c3902947f371188c7f1031e`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 4.2 MB (4209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f72515d4c5d212a324ec229420489d6c710211c685a20f842fe5ea2e2fb34f`  
		Last Modified: Tue, 18 Nov 2025 05:11:29 GMT  
		Size: 34.7 MB (34738444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101cbd53c83f0cf349b57fb7bd41cc20e9f6eb49387c77318fdef384138cc278`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc836501634abe40f87ab2e14b52ed1c6de8820cb1da01b09ad98e676e32190`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd6170440be24604d56cc5a5c6d054cba6f30789ef9229f99750120d2a142d`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:afc8298dddf93da25a7191a5d81662c4ed8f38a7880e02448f76a04c88006937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3df9ecbbfd4cb8ab05256d7313aeac34fa9c68e0b8138b4ce5cde4cdb399ae9`

```dockerfile
```

-	Layers:
	-	`sha256:4e93229cbe69b9230a76ea839dc174683f524a92a185cf722b3f6124328208d7`  
		Last Modified: Tue, 18 Nov 2025 07:40:01 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafdaf1b46ed4337e976046b7d22356e5a0f195b85a26df2ab25a9d91cb6a836`  
		Last Modified: Tue, 18 Nov 2025 07:40:02 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6748155e4bf4ca39277c0595e3e47864a54a7a4004ea5a42525dd731a19a5491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c25d7492e212b78522d62d01eb3be25f0dbdb5965f0a5675a681b63940e68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:01:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 18 Nov 2025 04:01:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:01:47 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:01:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:01:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b194a9e073f876b514613d7bde6ad1a612e4d90a6fc0c4eebffb6cd087167443`  
		Last Modified: Tue, 18 Nov 2025 04:02:03 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce9783893a3eb496a64a86fa500b1448f680b011eea1804f0991a8363dbb293`  
		Last Modified: Tue, 18 Nov 2025 04:02:07 GMT  
		Size: 33.1 MB (33097603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44562d79b790d29596e1f97153279aded1d4202e94063adc72b1735fe7fb8c5e`  
		Last Modified: Tue, 18 Nov 2025 04:02:02 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736b3a5e769b95d39d930a5b03efc9bec1a0a8ee2edea04a01330a0f1aedbf8a`  
		Last Modified: Tue, 18 Nov 2025 04:02:03 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a22c098fc67c0be11bf18255c461488255610da6c5db59be41bce2ea80e0b6`  
		Last Modified: Tue, 18 Nov 2025 04:02:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:e2399aad35377c1432366dd0ec525d4847a54cbe2edcd815ea70e66f4bee2cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf78956c3e21c0efd35971234ede0afa7964c3b5f36be6bb31fe833c47b07cd`

```dockerfile
```

-	Layers:
	-	`sha256:b4fddc57df683735be50ac06ed1445338745bf0031e3b764b55fb9dc2efb0835`  
		Last Modified: Tue, 18 Nov 2025 04:42:07 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436029456751dae600fa277741697595ab1d22d27e55a84ca9d6137e93a78a64`  
		Last Modified: Tue, 18 Nov 2025 04:42:07 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:342cb26f978f840423cc0a5b902f1f52ea2bd30f4fe24f573a876a65ea11f96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c96a5dc09cb1dbc405fe20d0219631a81e2942a0f4bec8767d56e9862725ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:28:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 18 Nov 2025 03:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:28:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:28:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:28:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e975aad8318aca4170a7fa3ef9a1fffd4507432c6b0bac018879f3f4afde4f`  
		Last Modified: Tue, 18 Nov 2025 03:29:04 GMT  
		Size: 4.2 MB (4210607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a8806f920702fe9baefe2e25da4ba39d25e0176fb80cfcc40448a934533452`  
		Last Modified: Tue, 18 Nov 2025 03:29:06 GMT  
		Size: 33.2 MB (33238100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c02ba5c51614553fdba4347b43d14e6c738d57d2eb68092945e7214afcf22c`  
		Last Modified: Tue, 18 Nov 2025 03:29:03 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4718396061feb9737fe7c087499e6f05fa025eca13cb64aa63c8471e978018b7`  
		Last Modified: Tue, 18 Nov 2025 03:29:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f328548464ad973a7e638abbb187ad3a19d64cb2abee1b34bf16b3dea236`  
		Last Modified: Tue, 18 Nov 2025 03:29:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:331090ae61e1e3fc51e741c54179a1636f7119ad69f466f9cd4eab1b8d4cb4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79789ed85d1cb59ddd8b441c0a0ffec43058ace58d605572e89c7d4c38dcd0a1`

```dockerfile
```

-	Layers:
	-	`sha256:03be267fbf04d42590712397fb5b734e27782be4c97c25ee6dba2cf99d86cc7c`  
		Last Modified: Tue, 18 Nov 2025 04:42:11 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc70a5607b52a19f2c3d7d03c7bd310032ad24e2fb8f5414b6aad7e3ddee539`  
		Last Modified: Tue, 18 Nov 2025 04:42:12 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:21 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:78c1c40d2c71f8bfd127862e5b96a1a366d39d081a4679107bb2bbc6e9ce7eb1
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
$ docker pull chronograf@sha256:c32bb8ad1ea434871eb8ef30f4939a85b8a4a466f68c9d84f861ef015f1c793c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda210c5adc84b59574a05f318b600b3fc41031bec0ab76e78834ec72866a918`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:11:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 18 Nov 2025 05:11:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:11:09 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:11:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:11:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903b4b7ce27b9621d75e24e8defd50b933d8b556c3902947f371188c7f1031e`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 4.2 MB (4209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f72515d4c5d212a324ec229420489d6c710211c685a20f842fe5ea2e2fb34f`  
		Last Modified: Tue, 18 Nov 2025 05:11:29 GMT  
		Size: 34.7 MB (34738444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101cbd53c83f0cf349b57fb7bd41cc20e9f6eb49387c77318fdef384138cc278`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc836501634abe40f87ab2e14b52ed1c6de8820cb1da01b09ad98e676e32190`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd6170440be24604d56cc5a5c6d054cba6f30789ef9229f99750120d2a142d`  
		Last Modified: Tue, 18 Nov 2025 05:11:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:afc8298dddf93da25a7191a5d81662c4ed8f38a7880e02448f76a04c88006937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3df9ecbbfd4cb8ab05256d7313aeac34fa9c68e0b8138b4ce5cde4cdb399ae9`

```dockerfile
```

-	Layers:
	-	`sha256:4e93229cbe69b9230a76ea839dc174683f524a92a185cf722b3f6124328208d7`  
		Last Modified: Tue, 18 Nov 2025 07:40:01 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafdaf1b46ed4337e976046b7d22356e5a0f195b85a26df2ab25a9d91cb6a836`  
		Last Modified: Tue, 18 Nov 2025 07:40:02 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6748155e4bf4ca39277c0595e3e47864a54a7a4004ea5a42525dd731a19a5491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c25d7492e212b78522d62d01eb3be25f0dbdb5965f0a5675a681b63940e68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:01:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 18 Nov 2025 04:01:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:01:47 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:01:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:01:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:01:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b194a9e073f876b514613d7bde6ad1a612e4d90a6fc0c4eebffb6cd087167443`  
		Last Modified: Tue, 18 Nov 2025 04:02:03 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce9783893a3eb496a64a86fa500b1448f680b011eea1804f0991a8363dbb293`  
		Last Modified: Tue, 18 Nov 2025 04:02:07 GMT  
		Size: 33.1 MB (33097603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44562d79b790d29596e1f97153279aded1d4202e94063adc72b1735fe7fb8c5e`  
		Last Modified: Tue, 18 Nov 2025 04:02:02 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736b3a5e769b95d39d930a5b03efc9bec1a0a8ee2edea04a01330a0f1aedbf8a`  
		Last Modified: Tue, 18 Nov 2025 04:02:03 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a22c098fc67c0be11bf18255c461488255610da6c5db59be41bce2ea80e0b6`  
		Last Modified: Tue, 18 Nov 2025 04:02:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:e2399aad35377c1432366dd0ec525d4847a54cbe2edcd815ea70e66f4bee2cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf78956c3e21c0efd35971234ede0afa7964c3b5f36be6bb31fe833c47b07cd`

```dockerfile
```

-	Layers:
	-	`sha256:b4fddc57df683735be50ac06ed1445338745bf0031e3b764b55fb9dc2efb0835`  
		Last Modified: Tue, 18 Nov 2025 04:42:07 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436029456751dae600fa277741697595ab1d22d27e55a84ca9d6137e93a78a64`  
		Last Modified: Tue, 18 Nov 2025 04:42:07 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:342cb26f978f840423cc0a5b902f1f52ea2bd30f4fe24f573a876a65ea11f96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c96a5dc09cb1dbc405fe20d0219631a81e2942a0f4bec8767d56e9862725ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:28:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 18 Nov 2025 03:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:28:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:28:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:28:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:28:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e975aad8318aca4170a7fa3ef9a1fffd4507432c6b0bac018879f3f4afde4f`  
		Last Modified: Tue, 18 Nov 2025 03:29:04 GMT  
		Size: 4.2 MB (4210607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a8806f920702fe9baefe2e25da4ba39d25e0176fb80cfcc40448a934533452`  
		Last Modified: Tue, 18 Nov 2025 03:29:06 GMT  
		Size: 33.2 MB (33238100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c02ba5c51614553fdba4347b43d14e6c738d57d2eb68092945e7214afcf22c`  
		Last Modified: Tue, 18 Nov 2025 03:29:03 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4718396061feb9737fe7c087499e6f05fa025eca13cb64aa63c8471e978018b7`  
		Last Modified: Tue, 18 Nov 2025 03:29:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f328548464ad973a7e638abbb187ad3a19d64cb2abee1b34bf16b3dea236`  
		Last Modified: Tue, 18 Nov 2025 03:29:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:331090ae61e1e3fc51e741c54179a1636f7119ad69f466f9cd4eab1b8d4cb4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79789ed85d1cb59ddd8b441c0a0ffec43058ace58d605572e89c7d4c38dcd0a1`

```dockerfile
```

-	Layers:
	-	`sha256:03be267fbf04d42590712397fb5b734e27782be4c97c25ee6dba2cf99d86cc7c`  
		Last Modified: Tue, 18 Nov 2025 04:42:11 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc70a5607b52a19f2c3d7d03c7bd310032ad24e2fb8f5414b6aad7e3ddee539`  
		Last Modified: Tue, 18 Nov 2025 04:42:12 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:21 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:2d4c1f1648159749ceb5056d4bcd77e7245ad3e60bc128963d8a70d1bdb899e7
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
$ docker pull chronograf@sha256:078f3a3afdc406cd286ec58d4d15b413b130b5737c40ee7309a78f08962b5204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8eab196f6f310cba0c1756113be6c6ff275c29054a67cbc24487e46280698a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:11:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 18 Nov 2025 05:11:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:11:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:11:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:11:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d96406e2f1b6af3145b21bb0614b88c555bcd4813615687976d0b633129b96c`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba33adc704b9c12a2f0a5820ff1b60e051ec6c598dd5fd3910e6f323c756e543`  
		Last Modified: Tue, 18 Nov 2025 05:11:39 GMT  
		Size: 34.4 MB (34364377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248ea9c1f77292342e0aba5e9507c2cf62be65d8887690d79c1d00aeb86592fd`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525f59857c1cd14efcce9ef9ff9f52cf3980e705f1c3a9cc52970c6be9872600`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7c85b0ae898eaa6ff55506b125a189c25d70f789ec542dd86e52488c22db83`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:4334926657bba9ed5a2ecc70c83b36712b46d95678d643eca32c4ffd16a8888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed81a768cb4fb28e6410b785e7e47fdb8d5b78e46d32a96de6b5c183cddbafad`

```dockerfile
```

-	Layers:
	-	`sha256:107a29d4eb18595bc4ec4d904d99db0e78554e1e49cfca5a567fad0def33cbb7`  
		Last Modified: Tue, 18 Nov 2025 07:40:10 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5558c06fe51cb78a2f73382f0ef76d57adbb97df7609822153cc91fcd346a8`  
		Last Modified: Tue, 18 Nov 2025 07:40:11 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:dac03e70d04165cb4f1e4d668c62546ac3525c1f250fe6b3c0720721ffac7418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68c119b33debe2247479f8c4843e741fa6ab192c7c3e5d22851c2ce2f1ae786`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:02:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 18 Nov 2025 04:03:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:03:00 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac745f2e7b8cffb577a80644a0caade9d66ea5e627ad0ba473f23361a2f91f8e`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 4.5 MB (4490193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6546d146579a252b8dd15e929863d6add7b9cdd14aeb82e383e671b9d3be7a74`  
		Last Modified: Tue, 18 Nov 2025 04:03:17 GMT  
		Size: 32.5 MB (32534921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d8353bbab8489803321b26b44b593ca349c3b681fb5f8f0ad85f85d4a30ecf`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5081bf97e6c93eb9edf78a8534a27a0cf219cc69e1505683b8120f2e1124dc5`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892db2d1de4cfe97114a9b34e0d0b350418af012bfeff4bf7c42db078a7c55cf`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:774db87de3c8a734487452c61da445921193cb66a1a554e9dec2863ed2867d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad06000b9fe0772ba29cd9cab3d95d065ad0e784ded522f6637650f39c9a6b1`

```dockerfile
```

-	Layers:
	-	`sha256:c67e8c2b3029b0be696537c2c61c528bc3e90f2bfc8ef0e293a0427a34812d17`  
		Last Modified: Tue, 18 Nov 2025 04:42:22 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8e1d6f8d11e794ea6c5962367d2b022ae9354b6263084b5c584c9c1ad26d1a`  
		Last Modified: Tue, 18 Nov 2025 04:42:23 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5901e8f3e2e818af20bf216107200083ef0e53eb82d79fb0e7e0b06f1809e97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9661bf08b88edce955e28ba165e8d8047f585c43fafabbd99aff2a06ebebecd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:29:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 18 Nov 2025 03:29:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:29:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:29:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:29:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aefb8cc15c4172a8315a394899c0be4d5491f2eb5496f589c4824ee88661901`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 5.2 MB (5208191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ad6b6a22fa86b99baf91888288bc4d6dcc2a175758b8a7c90e31d802df970`  
		Last Modified: Tue, 18 Nov 2025 03:30:10 GMT  
		Size: 32.4 MB (32429546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c871f6b33582df9eff5101476314b818b3180f041bd1fb248e42424d60128ef1`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654aa59349743a70a7055de993cea5f6310cd558953516cd541f79bcb28ba44b`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adce82a3b7cd12fa8f366e4e93800c2859d9a3fb81e9e169c1305859a3f815a`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:5771c424b947e3c18f2458adf39de73c72d4745ae0fe5a87233f2965b716a0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a322f2d253faf43ad847bd77ff8e4a0dbb47a68dcb5e1e56c08fc2436184e88f`

```dockerfile
```

-	Layers:
	-	`sha256:48d1cf79a89dfc16bd84c8cc29a4a5f1073104d0f0504c7ffef57ecf4218ea3c`  
		Last Modified: Tue, 18 Nov 2025 04:42:26 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22820e61bb8174a0286078ddf93df764d760f87d128b924b2630086d54947e61`  
		Last Modified: Tue, 18 Nov 2025 04:42:27 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Wed, 08 Oct 2025 23:01:11 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Wed, 08 Oct 2025 23:01:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Thu, 09 Oct 2025 00:38:34 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Thu, 09 Oct 2025 00:38:35 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:2d4c1f1648159749ceb5056d4bcd77e7245ad3e60bc128963d8a70d1bdb899e7
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
$ docker pull chronograf@sha256:078f3a3afdc406cd286ec58d4d15b413b130b5737c40ee7309a78f08962b5204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8eab196f6f310cba0c1756113be6c6ff275c29054a67cbc24487e46280698a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:11:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 18 Nov 2025 05:11:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:11:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:11:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:11:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:11:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d96406e2f1b6af3145b21bb0614b88c555bcd4813615687976d0b633129b96c`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 5.2 MB (5224274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba33adc704b9c12a2f0a5820ff1b60e051ec6c598dd5fd3910e6f323c756e543`  
		Last Modified: Tue, 18 Nov 2025 05:11:39 GMT  
		Size: 34.4 MB (34364377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248ea9c1f77292342e0aba5e9507c2cf62be65d8887690d79c1d00aeb86592fd`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525f59857c1cd14efcce9ef9ff9f52cf3980e705f1c3a9cc52970c6be9872600`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7c85b0ae898eaa6ff55506b125a189c25d70f789ec542dd86e52488c22db83`  
		Last Modified: Tue, 18 Nov 2025 05:11:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4334926657bba9ed5a2ecc70c83b36712b46d95678d643eca32c4ffd16a8888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed81a768cb4fb28e6410b785e7e47fdb8d5b78e46d32a96de6b5c183cddbafad`

```dockerfile
```

-	Layers:
	-	`sha256:107a29d4eb18595bc4ec4d904d99db0e78554e1e49cfca5a567fad0def33cbb7`  
		Last Modified: Tue, 18 Nov 2025 07:40:10 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5558c06fe51cb78a2f73382f0ef76d57adbb97df7609822153cc91fcd346a8`  
		Last Modified: Tue, 18 Nov 2025 07:40:11 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:dac03e70d04165cb4f1e4d668c62546ac3525c1f250fe6b3c0720721ffac7418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68c119b33debe2247479f8c4843e741fa6ab192c7c3e5d22851c2ce2f1ae786`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:02:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 18 Nov 2025 04:03:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:03:00 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:03:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac745f2e7b8cffb577a80644a0caade9d66ea5e627ad0ba473f23361a2f91f8e`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 4.5 MB (4490193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6546d146579a252b8dd15e929863d6add7b9cdd14aeb82e383e671b9d3be7a74`  
		Last Modified: Tue, 18 Nov 2025 04:03:17 GMT  
		Size: 32.5 MB (32534921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d8353bbab8489803321b26b44b593ca349c3b681fb5f8f0ad85f85d4a30ecf`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5081bf97e6c93eb9edf78a8534a27a0cf219cc69e1505683b8120f2e1124dc5`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892db2d1de4cfe97114a9b34e0d0b350418af012bfeff4bf7c42db078a7c55cf`  
		Last Modified: Tue, 18 Nov 2025 04:03:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:774db87de3c8a734487452c61da445921193cb66a1a554e9dec2863ed2867d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad06000b9fe0772ba29cd9cab3d95d065ad0e784ded522f6637650f39c9a6b1`

```dockerfile
```

-	Layers:
	-	`sha256:c67e8c2b3029b0be696537c2c61c528bc3e90f2bfc8ef0e293a0427a34812d17`  
		Last Modified: Tue, 18 Nov 2025 04:42:22 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8e1d6f8d11e794ea6c5962367d2b022ae9354b6263084b5c584c9c1ad26d1a`  
		Last Modified: Tue, 18 Nov 2025 04:42:23 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5901e8f3e2e818af20bf216107200083ef0e53eb82d79fb0e7e0b06f1809e97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9661bf08b88edce955e28ba165e8d8047f585c43fafabbd99aff2a06ebebecd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:29:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 18 Nov 2025 03:29:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:29:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:29:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:29:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aefb8cc15c4172a8315a394899c0be4d5491f2eb5496f589c4824ee88661901`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 5.2 MB (5208191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ad6b6a22fa86b99baf91888288bc4d6dcc2a175758b8a7c90e31d802df970`  
		Last Modified: Tue, 18 Nov 2025 03:30:10 GMT  
		Size: 32.4 MB (32429546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c871f6b33582df9eff5101476314b818b3180f041bd1fb248e42424d60128ef1`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654aa59349743a70a7055de993cea5f6310cd558953516cd541f79bcb28ba44b`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adce82a3b7cd12fa8f366e4e93800c2859d9a3fb81e9e169c1305859a3f815a`  
		Last Modified: Tue, 18 Nov 2025 03:30:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5771c424b947e3c18f2458adf39de73c72d4745ae0fe5a87233f2965b716a0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a322f2d253faf43ad847bd77ff8e4a0dbb47a68dcb5e1e56c08fc2436184e88f`

```dockerfile
```

-	Layers:
	-	`sha256:48d1cf79a89dfc16bd84c8cc29a4a5f1073104d0f0504c7ffef57ecf4218ea3c`  
		Last Modified: Tue, 18 Nov 2025 04:42:26 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22820e61bb8174a0286078ddf93df764d760f87d128b924b2630086d54947e61`  
		Last Modified: Tue, 18 Nov 2025 04:42:27 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Wed, 08 Oct 2025 23:01:11 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Wed, 08 Oct 2025 23:01:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Thu, 09 Oct 2025 00:38:34 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Thu, 09 Oct 2025 00:38:35 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:469642389a30e6d56be945c0039d0c6d07dbf94f4a3e54adcecf0324c0a570c4
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
$ docker pull chronograf@sha256:5fc7c19ebbcf3230b02079c5c0af1a271427f1f2634fdb00f88cfe28793a96c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664091bfb98b6bd38e5afc84e4cb731f834959af02edd0e97a19ef0bfb7e5ffa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:11:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 18 Nov 2025 05:11:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:11:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:11:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:11:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfefd72b9fac409c0aa314cd4e8b2222369f272614b6aff77e7a496c177001a`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 5.2 MB (5224218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7305bdc7fd29e3f156e9d13924eed8301a5a4bd641e57f5f94a52d8cb8951e77`  
		Last Modified: Tue, 18 Nov 2025 05:12:18 GMT  
		Size: 35.0 MB (35011728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f8ef0112efca62761ca57ac6e2175983bdd1897355f74fe911820020d15dd5`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6c4202406e3539d707ea17a85c4167d3d60d09d251ffe54891fc6ccb90f7c9`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f2a0df559bed83333514af4016c801b062ae018ed09f5d861859f09870f6e0`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:ee2392f19904bec431518a1d6052f340685ee17dbb5b3235f0017d433682f4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dbf6ac5dbd53ba984c82bad213e6a252e48d5fe7eeac533cd8f2e98fdda6ed`

```dockerfile
```

-	Layers:
	-	`sha256:1b83280fc401a0932145b1134897397d1ad13b935256ecdec20863f5769ddf04`  
		Last Modified: Tue, 18 Nov 2025 07:40:18 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0009d705499773327702c130d894efaa93d8b849838f94e3c3773b43db7727`  
		Last Modified: Tue, 18 Nov 2025 07:40:19 GMT  
		Size: 15.8 KB (15765 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3efdc7aa1147f3097bb775acee7d66bf2ef01332e57f80763d1cf4f62266bb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154bcc831630f11592d4a399c7731d4e8cea5d87ef087029e42a60e2ea873812`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:08:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 18 Nov 2025 04:08:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:08:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:08:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:08:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e3796737cf6025ac50cfc079db045dc27f7130aa29cffbac0bb61eb4113f4`  
		Last Modified: Tue, 18 Nov 2025 04:09:02 GMT  
		Size: 4.5 MB (4490174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b4ad5052673676a5e5852b79ef81e3280fee5b4288d8db81cc02cd227149df`  
		Last Modified: Tue, 18 Nov 2025 04:09:04 GMT  
		Size: 33.3 MB (33311571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a32a6c79537faa0ae3a9793d8b8f03d78f1a52781fccac33858c17b625b1eb`  
		Last Modified: Tue, 18 Nov 2025 04:09:01 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073319cead62b278beac7b8859184d528ff0b62b81467d2d34cd70b0daec0789`  
		Last Modified: Tue, 18 Nov 2025 04:09:01 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d95f61dc4d7540b4579465bd11b2d766bf0c6508a5ac57650d31baf31f4076`  
		Last Modified: Tue, 18 Nov 2025 04:09:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:be3fdfad0f89e242f36da92710de078aa37de00f55a910131db97cee3788e9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a3572270fece7de6d01c28966e7ea1faf7a82cb6bc5e6c9d9a7d8acd3db53c`

```dockerfile
```

-	Layers:
	-	`sha256:731ce55a37cd956d6868597ae55ee57c8e5870433432a67dda04931ce9fed76b`  
		Last Modified: Tue, 18 Nov 2025 04:42:35 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d131b8dc1edcafbc47bc06bc76c8f9823a194b5309a1600db92a17f6337134fc`  
		Last Modified: Tue, 18 Nov 2025 04:42:35 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:db82e7cb69e75202b07fc5cc77c49068bce5ab87fc9ad8948a87f887b8fcabed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdca592b3498a6c77f3300370a6791a6bd4d98db3021776720e77524c267c5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:30:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 18 Nov 2025 03:30:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:30:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:30:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:30:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b904e8a61b1be20cc3c3eaa7fca963bee6b30700098a310c8fc0d7eb1f95af12`  
		Last Modified: Tue, 18 Nov 2025 03:31:14 GMT  
		Size: 5.2 MB (5208156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8baf37b091caa3abbb194d03fc307eba9e1b05f1c9ca1ffdd8bb40026f665d`  
		Last Modified: Tue, 18 Nov 2025 03:31:20 GMT  
		Size: 33.2 MB (33182145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42980029e6385121f26330516de524ae192b62501b55c99555556f4da1b296a`  
		Last Modified: Tue, 18 Nov 2025 03:31:15 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950d5ad9ff99c2cae2435b54c3dd9c3105b4c004166dfc6457c674bd0e81e48`  
		Last Modified: Tue, 18 Nov 2025 03:31:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fba4ee5bd232835a95043b86349860e6be3bd5eceb72e75b522578916dca6`  
		Last Modified: Tue, 18 Nov 2025 03:31:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:6f3346a65d46520be009eef6134f3e942d1fb717f6c22a16e4b8c287043bf958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71901a1ded3dedc253d57fa6352a1c91f770e121a548cc08adee392ee550682f`

```dockerfile
```

-	Layers:
	-	`sha256:3624ace9bee6a90624e5e2fe524aa29d7d115a0b2cf2ae87c6a50729ecb3eefb`  
		Last Modified: Tue, 18 Nov 2025 04:42:39 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9405fb9ea9819f5026583be8966fa9e3636c0fded66678f4f13e30e849d83c92`  
		Last Modified: Tue, 18 Nov 2025 04:42:40 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:26 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:469642389a30e6d56be945c0039d0c6d07dbf94f4a3e54adcecf0324c0a570c4
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
$ docker pull chronograf@sha256:5fc7c19ebbcf3230b02079c5c0af1a271427f1f2634fdb00f88cfe28793a96c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664091bfb98b6bd38e5afc84e4cb731f834959af02edd0e97a19ef0bfb7e5ffa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:11:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 18 Nov 2025 05:11:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:11:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:11:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:11:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfefd72b9fac409c0aa314cd4e8b2222369f272614b6aff77e7a496c177001a`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 5.2 MB (5224218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7305bdc7fd29e3f156e9d13924eed8301a5a4bd641e57f5f94a52d8cb8951e77`  
		Last Modified: Tue, 18 Nov 2025 05:12:18 GMT  
		Size: 35.0 MB (35011728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f8ef0112efca62761ca57ac6e2175983bdd1897355f74fe911820020d15dd5`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6c4202406e3539d707ea17a85c4167d3d60d09d251ffe54891fc6ccb90f7c9`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f2a0df559bed83333514af4016c801b062ae018ed09f5d861859f09870f6e0`  
		Last Modified: Tue, 18 Nov 2025 05:12:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:ee2392f19904bec431518a1d6052f340685ee17dbb5b3235f0017d433682f4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dbf6ac5dbd53ba984c82bad213e6a252e48d5fe7eeac533cd8f2e98fdda6ed`

```dockerfile
```

-	Layers:
	-	`sha256:1b83280fc401a0932145b1134897397d1ad13b935256ecdec20863f5769ddf04`  
		Last Modified: Tue, 18 Nov 2025 07:40:18 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0009d705499773327702c130d894efaa93d8b849838f94e3c3773b43db7727`  
		Last Modified: Tue, 18 Nov 2025 07:40:19 GMT  
		Size: 15.8 KB (15765 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3efdc7aa1147f3097bb775acee7d66bf2ef01332e57f80763d1cf4f62266bb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154bcc831630f11592d4a399c7731d4e8cea5d87ef087029e42a60e2ea873812`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:08:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 18 Nov 2025 04:08:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:08:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:08:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:08:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e3796737cf6025ac50cfc079db045dc27f7130aa29cffbac0bb61eb4113f4`  
		Last Modified: Tue, 18 Nov 2025 04:09:02 GMT  
		Size: 4.5 MB (4490174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b4ad5052673676a5e5852b79ef81e3280fee5b4288d8db81cc02cd227149df`  
		Last Modified: Tue, 18 Nov 2025 04:09:04 GMT  
		Size: 33.3 MB (33311571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a32a6c79537faa0ae3a9793d8b8f03d78f1a52781fccac33858c17b625b1eb`  
		Last Modified: Tue, 18 Nov 2025 04:09:01 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073319cead62b278beac7b8859184d528ff0b62b81467d2d34cd70b0daec0789`  
		Last Modified: Tue, 18 Nov 2025 04:09:01 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d95f61dc4d7540b4579465bd11b2d766bf0c6508a5ac57650d31baf31f4076`  
		Last Modified: Tue, 18 Nov 2025 04:09:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:be3fdfad0f89e242f36da92710de078aa37de00f55a910131db97cee3788e9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a3572270fece7de6d01c28966e7ea1faf7a82cb6bc5e6c9d9a7d8acd3db53c`

```dockerfile
```

-	Layers:
	-	`sha256:731ce55a37cd956d6868597ae55ee57c8e5870433432a67dda04931ce9fed76b`  
		Last Modified: Tue, 18 Nov 2025 04:42:35 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d131b8dc1edcafbc47bc06bc76c8f9823a194b5309a1600db92a17f6337134fc`  
		Last Modified: Tue, 18 Nov 2025 04:42:35 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:db82e7cb69e75202b07fc5cc77c49068bce5ab87fc9ad8948a87f887b8fcabed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdca592b3498a6c77f3300370a6791a6bd4d98db3021776720e77524c267c5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:30:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 18 Nov 2025 03:30:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:30:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:30:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:30:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b904e8a61b1be20cc3c3eaa7fca963bee6b30700098a310c8fc0d7eb1f95af12`  
		Last Modified: Tue, 18 Nov 2025 03:31:14 GMT  
		Size: 5.2 MB (5208156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8baf37b091caa3abbb194d03fc307eba9e1b05f1c9ca1ffdd8bb40026f665d`  
		Last Modified: Tue, 18 Nov 2025 03:31:20 GMT  
		Size: 33.2 MB (33182145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42980029e6385121f26330516de524ae192b62501b55c99555556f4da1b296a`  
		Last Modified: Tue, 18 Nov 2025 03:31:15 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950d5ad9ff99c2cae2435b54c3dd9c3105b4c004166dfc6457c674bd0e81e48`  
		Last Modified: Tue, 18 Nov 2025 03:31:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fba4ee5bd232835a95043b86349860e6be3bd5eceb72e75b522578916dca6`  
		Last Modified: Tue, 18 Nov 2025 03:31:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:6f3346a65d46520be009eef6134f3e942d1fb717f6c22a16e4b8c287043bf958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71901a1ded3dedc253d57fa6352a1c91f770e121a548cc08adee392ee550682f`

```dockerfile
```

-	Layers:
	-	`sha256:3624ace9bee6a90624e5e2fe524aa29d7d115a0b2cf2ae87c6a50729ecb3eefb`  
		Last Modified: Tue, 18 Nov 2025 04:42:39 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9405fb9ea9819f5026583be8966fa9e3636c0fded66678f4f13e30e849d83c92`  
		Last Modified: Tue, 18 Nov 2025 04:42:40 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:26 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1140faa8c1bb598f1660c359a5db8fc40bd9f325109f5983156a835725548890
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
$ docker pull chronograf@sha256:9e7f5b612bbdb4be8675320e3ff7d3bf1c942ad06970c3f170d2c1dd329792a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ced03eba5efa1482e1606ca10c179fccef17967909c68b4e339a4d855a5c5fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:11:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 05:12:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 05:12:01 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 05:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:12:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff136bf2c7928ce0501ad7b858da691f60acd2ce2dd42c72ed7d0e879ece89ed`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 7.9 MB (7878770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22554aeaa4ff175a76313f43728ecc9641a4ff235f2f4426cb058478def98ba`  
		Last Modified: Tue, 18 Nov 2025 05:12:24 GMT  
		Size: 49.3 MB (49276640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7443cf8f1612d0ed8cf6c8e4d3b107b6514849725b1f82366c4cd453226aef6`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b57c07510327eb66bc1223c4af94766640a29095f6a5d17a91fa16e2148a21`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0413830ddd1599611bcaf02d2d9a43a716bb81c68202fe9e3b8f9c6b0905031`  
		Last Modified: Tue, 18 Nov 2025 05:12:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:165854fe1b463d83716d5698cffb26dc4dcdd9c1b99715c1dfed3535e5d92161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eae45dafd7ac73a76acf5ee362fe669a44a19aefc82736a176ded2fc045e4d`

```dockerfile
```

-	Layers:
	-	`sha256:3f3163a68ece5bd266953666fbfba8eddcd716dad3ce4dce620aaaf9cb60a224`  
		Last Modified: Tue, 18 Nov 2025 07:39:53 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5c611aa284b2ca4de5bb9c5a715eefbdb161a1b37f0aedcde60010234e4c4e`  
		Last Modified: Tue, 18 Nov 2025 07:39:54 GMT  
		Size: 16.1 KB (16083 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e1b13de5c8ec347837c2f5d250d1c2e80865aa445517aa06fc0bcc9e25b14abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25913dc7e88da6be5c53fe3140175f460a68f14f55856a3ebd12f5225ff6e164`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:17:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 04:17:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 04:17:38 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 04:17:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 04:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 04:17:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090570ce97227c589c84da564663c17964737bd94f351c5e4277316e34e3328b`  
		Last Modified: Tue, 18 Nov 2025 04:18:01 GMT  
		Size: 6.5 MB (6508158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe50b4d4c0e57c5aa2a1dafec359d48e73679be75d7397877754b72352c37d`  
		Last Modified: Tue, 18 Nov 2025 04:18:05 GMT  
		Size: 45.6 MB (45621855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c4be73ab28d36ccf2884b0f3b83104d0e8dee5b3601ff29c331c7a60ab522e`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a747e3b835cd3b4d70b4186e5553c8e17eb6b9fa414e0833a90a611809ade433`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4e072645cfa57704d9316047e0e0f4b5bea997852a9ed21594f25497c92cdc`  
		Last Modified: Tue, 18 Nov 2025 04:17:59 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:361e9a4e047048a444b66447bfc51ba18f4c997afa2098efd5f25584dd9ce6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720f507f08dca7cec9e10d8583e5ce39ffbee7cc1c5dcbb4c329ead1fa4457f1`

```dockerfile
```

-	Layers:
	-	`sha256:9731727bb4381d708af2f7544d7b7836f3a927ce6c31ed95e9c1542540aaf92c`  
		Last Modified: Tue, 18 Nov 2025 07:39:58 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d19a029240d6c9332e0318e801bb38c8157adae3b13448011f5277a5a78e2c`  
		Last Modified: Tue, 18 Nov 2025 07:39:59 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a779993306306e7db8b00934aaaae92e9edf407acf80aabe06b317ceee4a01e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df5325d525c2e46319bb640633ccfaf396d50b3d2938ddd6c7194707a33d287`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:31:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 18 Nov 2025 03:31:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 18 Nov 2025 03:31:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 18 Nov 2025 03:31:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:31:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:31:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0bc461d630893e7099423ad226893ab78dccbc7781b48cbf37e69cd79cd304`  
		Last Modified: Tue, 18 Nov 2025 03:32:19 GMT  
		Size: 7.7 MB (7691863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452cc9063d26f4676d73fa558b77cae141b38c2086158fba9cf70589d9c5e8c7`  
		Last Modified: Tue, 18 Nov 2025 03:32:26 GMT  
		Size: 47.1 MB (47066829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9a3e84192a601f3bd6d3e7ca86dfc08f8933f9ce86856aedd10f2bea4af6e8`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254bd12639bf9c90cc2cf8e22a186d95b868302652ed7b973f245791b4c945fd`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf36cb51c0dfd2bad204ce8824e65b8398e5ab5c176d88df6e621189c859214`  
		Last Modified: Tue, 18 Nov 2025 03:32:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:e7abf137713efc087412f366d56960a46c0ca78af03effaac752a900e34c506b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513d0ddddd8249f753232ffa801c47b1c5d8ce010f554e82c1ea03548467e3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5a44553c7ec7fe634d38a56ac68516bb68ccf2e228ec5cd99a6f6cadc695005e`  
		Last Modified: Tue, 18 Nov 2025 04:41:58 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7f4fe13eead8b0eacedc2971a58c309483750311e140db705345e06a33e877`  
		Last Modified: Tue, 18 Nov 2025 04:41:58 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
