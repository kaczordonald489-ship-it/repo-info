## `influxdb:latest`

```console
$ docker pull influxdb@sha256:b548ea6cdd265b4c28b305be5a93c4fc8b0d60583989598156895b80eefe29f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:80d06d6e62e4f1607126bfca0352e2b814ee0d5e2cb0d01b873ea0c3ff212a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771dee7da05d81f0e813477220d2c1fb328a25c6ed15c784b68ca47e3ae1aea5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:17:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 05:17:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 05:17:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:17:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 05:17:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 05:17:43 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 05:17:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 05:17:44 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:17:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 05:17:44 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 05:17:44 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 05:17:44 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 05:17:44 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083ac3dd494839df49da730b2ca808788a26c458e07803a53f6000b9914c008`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 9.8 MB (9796297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe79973373e0984f90d434906b24f59e09d3653e9b0a64ac501163cb06039b5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1f90322a676f797132f3760313f4ce5fef5e82214cbac2bae818934922be1d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd91bcec731380dc981617e7e6a27eff809dc77d80c891d64a1c432ea75e4dc`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0259fb23e7f74d9abb6dc12f70cb4d4625fe73b958700025e0ca624e76d431c`  
		Last Modified: Tue, 18 Nov 2025 05:18:22 GMT  
		Size: 100.2 MB (100244553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8513f44a5e4ba9d1fa3379e80a87a2b80fc40cb4f0a6022f49794e9cc6a8d5`  
		Last Modified: Tue, 18 Nov 2025 05:18:08 GMT  
		Size: 11.8 MB (11773792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d86a50f69f7d531e1c2cde43e54ea413d9d7f7799a4e6a3e83f72a22792951`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d57973d13ec346390d99f02c71f99a8a9faad512d116594b4eb34b74cf28d`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7325153cd01147116a63f1716e52cbbfb95cceff1bb7fe9729ee02cbfdbe731b`  
		Last Modified: Tue, 18 Nov 2025 05:18:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:b2e0a09a4a27fb5b377ef84ceba92851b41f9e99cc8d4253bd3dec91337049db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce77c8b808530a8d9ade8789ba9a0d0d6a8774bb8233631d66bfe7f337ba40ae`

```dockerfile
```

-	Layers:
	-	`sha256:35f5b1fc80bf8c5073e3a2e9b72ab62ca38d431e560b90e2c85b0b7521aee48b`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3cacf9519ba70a80483d2cb9194cffc0bde6187b2bf9f1f1a534adc089b6de7`  
		Last Modified: Tue, 18 Nov 2025 09:21:49 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebf4fd439730dadc92b3bc3f565966f49e0026098626fa0bbd1bf4dfcd3dc23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efe22d086df7cc3f7292fb6c0bfeb0bfd1e7dfe9b4ab2f531fb9e3cde7a74a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:45:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 03:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 03:46:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 03:46:04 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 03:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 03:46:06 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:46:06 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 03:46:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 03:46:06 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f18804d67ac382eaeac668698515f80ba62f0269c38f762d1afbd6be3db798`  
		Last Modified: Tue, 18 Nov 2025 03:46:34 GMT  
		Size: 9.6 MB (9626374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d00886f89ffaf07d35f7df7c3069dd3afe08bd1dd499c2d3deaddaba64ffad`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e659ab431338c547c1f98f68f92e58b74c5a951004693b9d9c5b87c329da5d`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59935d05743ffa02ec8f0b55b5ac55704d51555f71109d405d50fbc5e4c9ab`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 938.9 KB (938873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562febceec6f34093da512fc564ef68229e13b9cbc93448890ee3b25d4cba3ba`  
		Last Modified: Tue, 18 Nov 2025 03:46:41 GMT  
		Size: 96.0 MB (96039030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df32be97c38ea00ccc65fad323f679e2cdbdb0a21bc3401d70f74bcbf63496`  
		Last Modified: Tue, 18 Nov 2025 03:46:31 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbff83753ef6903833194bdec45bf87380a34a5c23aa0fc130e0bec7a4eab930`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fe0dc91a3c9b16f488df0eaa5967b709ea1bb28034bc8e0fd57b84fc6c45b`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80207f266c84c3062586aff91f93c2d37fbd833c2a4e160bb775fb6509c7daa6`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:39b6cf435fde35f43996921bf986e0b8c60bac78e8b3fb7cf079990262481998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475c2031479b1a92ed17ff24f69f4ce96e1ca85a835d81b9112d15ec2f01be2`

```dockerfile
```

-	Layers:
	-	`sha256:f75d415ae191d84746f95f4d12fa681a914b79864281212c05c5e323c2df000f`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca60a4fb48824c8d0e9b163faaa7aea6a7b0fe39e6e4faf8a38ecf3778f442e`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 33.7 KB (33678 bytes)  
		MIME: application/vnd.in-toto+json
