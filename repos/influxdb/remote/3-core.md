## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json
