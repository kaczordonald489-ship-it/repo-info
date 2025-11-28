## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json
