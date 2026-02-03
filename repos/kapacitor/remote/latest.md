## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:0b91b3acf44d3d578b205bd6e48c083a2a2cf0c81073e7108447f1c6d388dba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:316e124fcc0d4c8e8c51924d9a552fa576d6e92a567681e728c665516fd6d728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173824651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa34749cbffd8b4405edd652f3f54dbbdd69b39746aea1ee1f483f6c6e5eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:16:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:16:25 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:16:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:42 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c57012893e9c14b4ed9be8ff981779047a0270882fdc44dcbc62633cc7e32`  
		Last Modified: Thu, 15 Jan 2026 23:16:43 GMT  
		Size: 49.0 MB (48970775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001b6dd15f097a48f388ebd7ac53b24426780188e0003d01a3035e9949815cc`  
		Last Modified: Thu, 15 Jan 2026 23:16:44 GMT  
		Size: 88.2 MB (88212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd28eefc9be64c03f4386625be3e9e84b5e37b59f8707428be0e80b0ec1055e`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee239ae6aabfbd9dee2a137982ec91d496c77e9ce6911952947b5dc0b89fc328`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:da49a5d03519c9afb5a37fd68c601ad03da5677f937d098e972898b7823a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ee7c403e95a982b588095e396d65a9b77a92e00903498a70cbd69f4adee1c`

```dockerfile
```

-	Layers:
	-	`sha256:74b897cbd09ebfb85d02ae725b41a3a704f39493ae150df51c5b919bdf62e0ed`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81142b9e66372f3ee8c660975c4219a8830dd755a3164ae0925aa438a22389b`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:1eff3236806e63039ce16d5ec6b729e874f734640ef191027b81fe4c9330a151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f9c742c5c037ee1e884b24763997b778ee49fb4afea00038401930332285a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:21:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENV KAPACITOR_VERSION=1.8.2
# Thu, 15 Jan 2026 23:21:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
EXPOSE map[9092/tcp:{}]
# Thu, 15 Jan 2026 23:21:57 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 15 Jan 2026 23:21:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:21:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:57 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:29 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b066ac69fa615a156bc4b2cf1298e60a75122022abe5360dac459bcfdd4b7b`  
		Last Modified: Thu, 15 Jan 2026 23:22:13 GMT  
		Size: 47.2 MB (47213852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f523369fde43a4ea8bd398add7b37d189dc3d4d25f1bc37226edc54d76719`  
		Last Modified: Thu, 15 Jan 2026 23:22:14 GMT  
		Size: 82.0 MB (82009641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f9c520e751598daf66788cb9d9281379b9665fae8a19cb89b3823f4d1d07f`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd761fdd2bb99f3381484f0aee3ff1a23ba5989db64cdcc9d04980bd2e16d73`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:74947cdf7e133ce11495ec5896ab81f4fb893ec50cb7a27a9cc7c036f67d0607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f0a0901976304e95e4a6cf6fd576e90be6cace4b3f6ccd8e7346f36a21c39f`

```dockerfile
```

-	Layers:
	-	`sha256:f263e41f29ec2a97e31bc94888ca0b548221e2fa232e18d75c8744d4f7ce97b9`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe0a8ddc2a028f140c1a139ae06031fa36e9c2b0ec6949a12cb5a601f607fc0`  
		Last Modified: Thu, 15 Jan 2026 23:22:11 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
