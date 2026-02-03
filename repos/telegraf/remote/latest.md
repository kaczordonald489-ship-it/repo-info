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
