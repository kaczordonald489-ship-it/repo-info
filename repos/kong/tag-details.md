<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.5-ubuntu`](#kong285-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.4`](#kong34)
-	[`kong:3.4-ubuntu`](#kong34-ubuntu)
-	[`kong:3.4.2`](#kong342)
-	[`kong:3.4.2-ubuntu`](#kong342-ubuntu)
-	[`kong:3.8`](#kong38)
-	[`kong:3.8-ubuntu`](#kong38-ubuntu)
-	[`kong:3.8.0`](#kong380)
-	[`kong:3.8.0-ubuntu`](#kong380-ubuntu)
-	[`kong:3.9`](#kong39)
-	[`kong:3.9-ubuntu`](#kong39-ubuntu)
-	[`kong:3.9.1`](#kong391)
-	[`kong:3.9.1-ubuntu`](#kong391-ubuntu)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:99a0cc0c0c762e0062e7568c0fbfc10d70cf1fac33b4bf84dac40841a67a3771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7474a21392d2e6a4e3738835ddc7baeb06a673c2456882e360a24a02de06c1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185242834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9db1b80d0e52e804f704bd4efa6f8935020ca88597b41f541b98ec1e1c2354`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:49 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:49 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:49 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:49 GMT
ARG KONG_VERSION=2.8.5
# Thu, 15 Jan 2026 22:30:49 GMT
ENV KONG_VERSION=2.8.5
# Thu, 15 Jan 2026 22:30:49 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Thu, 15 Jan 2026 22:30:49 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 15 Jan 2026 22:31:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:31:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:27 GMT
USER kong
# Thu, 15 Jan 2026 22:31:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:31:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:31:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:31:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469704b8a4cb4850dc96a765abee708b58b39c048de0c052e8be3f3d6e9d1bde`  
		Last Modified: Thu, 15 Jan 2026 22:31:48 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40613b6802cf2adb3bdde3f0563ba7d1f2113d12a9b98cdd8329e57514eb08b5`  
		Last Modified: Thu, 15 Jan 2026 22:31:51 GMT  
		Size: 130.6 MB (130623319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c67a372ebf53096b4eea4bc9ce1bc0fddca4e7daadd0affcf368489e66105e`  
		Last Modified: Thu, 15 Jan 2026 22:31:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:a544534f432d8ba58605fcda02b8223286e1a68793fe9be7658457b625b341e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed7cda32ab8173d0e5264e343f451e1eba586fa215e7e381cc8331137f04cad`

```dockerfile
```

-	Layers:
	-	`sha256:a5ad827acad84111eb7921fe01fb14aa11c73fe0a2aa2397989d473ca77b9444`  
		Last Modified: Thu, 15 Jan 2026 22:31:48 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50b9e348839b383974b435264906b57be6615e0ba2e8772343841c0c4c7fa4`  
		Last Modified: Thu, 15 Jan 2026 22:31:47 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:99a0cc0c0c762e0062e7568c0fbfc10d70cf1fac33b4bf84dac40841a67a3771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7474a21392d2e6a4e3738835ddc7baeb06a673c2456882e360a24a02de06c1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185242834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9db1b80d0e52e804f704bd4efa6f8935020ca88597b41f541b98ec1e1c2354`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:49 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:49 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:49 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:49 GMT
ARG KONG_VERSION=2.8.5
# Thu, 15 Jan 2026 22:30:49 GMT
ENV KONG_VERSION=2.8.5
# Thu, 15 Jan 2026 22:30:49 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Thu, 15 Jan 2026 22:30:49 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 15 Jan 2026 22:31:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:31:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:27 GMT
USER kong
# Thu, 15 Jan 2026 22:31:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:31:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:31:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:31:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469704b8a4cb4850dc96a765abee708b58b39c048de0c052e8be3f3d6e9d1bde`  
		Last Modified: Thu, 15 Jan 2026 22:31:48 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40613b6802cf2adb3bdde3f0563ba7d1f2113d12a9b98cdd8329e57514eb08b5`  
		Last Modified: Thu, 15 Jan 2026 22:31:51 GMT  
		Size: 130.6 MB (130623319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c67a372ebf53096b4eea4bc9ce1bc0fddca4e7daadd0affcf368489e66105e`  
		Last Modified: Thu, 15 Jan 2026 22:31:47 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:a544534f432d8ba58605fcda02b8223286e1a68793fe9be7658457b625b341e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed7cda32ab8173d0e5264e343f451e1eba586fa215e7e381cc8331137f04cad`

```dockerfile
```

-	Layers:
	-	`sha256:a5ad827acad84111eb7921fe01fb14aa11c73fe0a2aa2397989d473ca77b9444`  
		Last Modified: Thu, 15 Jan 2026 22:31:48 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50b9e348839b383974b435264906b57be6615e0ba2e8772343841c0c4c7fa4`  
		Last Modified: Thu, 15 Jan 2026 22:31:47 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:9111d452bf4092245edd8b567d54c68f98c71d1a41eb0db84a2cb356af22da93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:2764b27f1f117d51e330d50f61db52d3800e650c2cfde0c0f94e15c06d3bf856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120411808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c4dd0ea26887a49e56fa59bd9569279239e7206ef03b0dfad5709310623ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:17 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:17 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:30:45 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
USER kong
# Thu, 15 Jan 2026 22:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:45 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb43f2c090f9362734ce2de3a4a83bb30decf80c1443d1847df95b79b1f6d9fc`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf064bb91096baef29f3dbf0b58457237673ed8809e734c26f03980d1d2cb1ab`  
		Last Modified: Thu, 15 Jan 2026 22:31:04 GMT  
		Size: 90.7 MB (90684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d53bd57a1e4c36ec63b892de6040a2a2ad99a810641f4ae3b14f30229281`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:77f2eca4db4c0d23f05356f9c9e05355c90d92d831e56b138a2115ea256dda15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f535ff2014658e105b80acdffbb397d09abe247f35020a13c586ad0e3f52c76`

```dockerfile
```

-	Layers:
	-	`sha256:318437fe8f73cce9afab408b58ca0c322060b5cb9c940e8797c88280140dc18a`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d05dadb7fb79dc281703a043b2b774da3f5a4a636337bd4220baa894b9eb79`  
		Last Modified: Thu, 15 Jan 2026 22:31:01 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9e558058ac6169e0a47ce01365ccbb5ae38fdf97be810582747e007ae96c81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118867702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c546477b1dd5cfeab175e87a6f81fab2b9e764a1d84e9c2931bcffbc27b6517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:21 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:32:50 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
USER kong
# Thu, 15 Jan 2026 22:32:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:50 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:32:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:32:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:32:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304f900a467aa61e07e6f11db6758e7a4c4c1c6da6979d0db9689e5bf73e059`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21bd5760326a990eda6c683d407beba3e5d32c5af5cfc912dcf108acdb864b2`  
		Last Modified: Thu, 15 Jan 2026 22:33:09 GMT  
		Size: 90.0 MB (90002592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbad4a31f221f9459047227092b06d9d87a6eb164d0d10f0f583116f715ae20`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:c4f0fd068c5196bc29d65a6b59407891306beec7604a3ed164900ad8188fbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac98a8bd40e76c88e79cd49c5e154c0d97aae550f25125d7238c8f79c91370d`

```dockerfile
```

-	Layers:
	-	`sha256:2e22ca6e0f57a5d72f509b43d1ddfe2be5bcd344b6a5df1af5b74af9db5a725c`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37823ba562e181ffb17b2465123b3f2c2579e4cfc3144b3c481c63397bcd76c2`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:006359bd9a1625dbebad43fda751bb9851b394686bfc8cee6e9d93b041263ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:ea07d14bfbba3adc5337e93f9532022fe164ce5cf493dfcdf749d8d38d4c5683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92277971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f5aba4c1f2dc2e6089308119adfd64ac6175305455424497ea34c91ba91c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:42 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:42 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:42 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:31:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
USER kong
# Thu, 15 Jan 2026 22:31:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:31:08 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:31:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:31:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0e71ec567dafc82f9a26f33506f67e23ba294e4dbe6b27de73bd88392a7e9`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95851f6441bbd0f5f9788340df95d53e219766679056619f090aa9a8c903e79`  
		Last Modified: Thu, 15 Jan 2026 22:31:22 GMT  
		Size: 62.7 MB (62740022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dede8248c1ebec209468671cd27f767862068057ebb706b9b7b73792bc5b29c5`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:d0d9ee5d35e3cd8ee5c3ccc5eeb8af273924bc92790c29358989b8ee2f2f64b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0d50d27d9f9e85adfbce006960ee4b6b0ec8e7dfff8a6d2bb633878178de`

```dockerfile
```

-	Layers:
	-	`sha256:b08f90a940ccf492c4bf8c9846504c4ccfaf8b6c3f2a1a16342b1e2f2340ca9e`  
		Last Modified: Thu, 15 Jan 2026 22:31:21 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:956db8aa9b642e8da3eb504c20472c0ca75334a86790cf425411616c438c69dd`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d5c3cf7171aed6ff0a6f82bc5069230942601a0bfd97684dfdfdde2e82ec8eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88583046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba5e14fea720da46c9d92e28922fdcc8871396caa188cbb43172309c7094e35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:52 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:33:17 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
USER kong
# Thu, 15 Jan 2026 22:33:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:17 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf70b612faec25c975e123e76f8846cb269cef9ad4b043a14c3afcc351232c`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514eb4e0ecc2bec3f614b60fa1fbb69f7ded6fb801a3b63ca5187f92495351f7`  
		Last Modified: Thu, 15 Jan 2026 22:33:33 GMT  
		Size: 61.2 MB (61198266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb647d3e5367c87e2202482e6815abaebbf63639e9bf90d841f4b9aef5bd0be`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:c8dd415c6c9253d1c7fcc93808679889183fdbade251c6816887591c8ec80fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8110f2a5a233d1b99b5e95a80bbace9615ce1e32f85a02583c0aa1bfd01c328d`

```dockerfile
```

-	Layers:
	-	`sha256:ad10c7eafd53f3768dd2abb1521a04edef6fb8de1ebbb1dbb6f174747d86dc44`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3802f104f039261cbb60e96645222259ad4b3dd713655594856a73e99a3d0051`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:006359bd9a1625dbebad43fda751bb9851b394686bfc8cee6e9d93b041263ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ea07d14bfbba3adc5337e93f9532022fe164ce5cf493dfcdf749d8d38d4c5683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92277971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f5aba4c1f2dc2e6089308119adfd64ac6175305455424497ea34c91ba91c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:42 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:42 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:42 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:31:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
USER kong
# Thu, 15 Jan 2026 22:31:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:31:08 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:31:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:31:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0e71ec567dafc82f9a26f33506f67e23ba294e4dbe6b27de73bd88392a7e9`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95851f6441bbd0f5f9788340df95d53e219766679056619f090aa9a8c903e79`  
		Last Modified: Thu, 15 Jan 2026 22:31:22 GMT  
		Size: 62.7 MB (62740022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dede8248c1ebec209468671cd27f767862068057ebb706b9b7b73792bc5b29c5`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d0d9ee5d35e3cd8ee5c3ccc5eeb8af273924bc92790c29358989b8ee2f2f64b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0d50d27d9f9e85adfbce006960ee4b6b0ec8e7dfff8a6d2bb633878178de`

```dockerfile
```

-	Layers:
	-	`sha256:b08f90a940ccf492c4bf8c9846504c4ccfaf8b6c3f2a1a16342b1e2f2340ca9e`  
		Last Modified: Thu, 15 Jan 2026 22:31:21 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:956db8aa9b642e8da3eb504c20472c0ca75334a86790cf425411616c438c69dd`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d5c3cf7171aed6ff0a6f82bc5069230942601a0bfd97684dfdfdde2e82ec8eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88583046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba5e14fea720da46c9d92e28922fdcc8871396caa188cbb43172309c7094e35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:52 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:33:17 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
USER kong
# Thu, 15 Jan 2026 22:33:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:17 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf70b612faec25c975e123e76f8846cb269cef9ad4b043a14c3afcc351232c`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514eb4e0ecc2bec3f614b60fa1fbb69f7ded6fb801a3b63ca5187f92495351f7`  
		Last Modified: Thu, 15 Jan 2026 22:33:33 GMT  
		Size: 61.2 MB (61198266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb647d3e5367c87e2202482e6815abaebbf63639e9bf90d841f4b9aef5bd0be`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c8dd415c6c9253d1c7fcc93808679889183fdbade251c6816887591c8ec80fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8110f2a5a233d1b99b5e95a80bbace9615ce1e32f85a02583c0aa1bfd01c328d`

```dockerfile
```

-	Layers:
	-	`sha256:ad10c7eafd53f3768dd2abb1521a04edef6fb8de1ebbb1dbb6f174747d86dc44`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3802f104f039261cbb60e96645222259ad4b3dd713655594856a73e99a3d0051`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:006359bd9a1625dbebad43fda751bb9851b394686bfc8cee6e9d93b041263ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:ea07d14bfbba3adc5337e93f9532022fe164ce5cf493dfcdf749d8d38d4c5683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92277971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f5aba4c1f2dc2e6089308119adfd64ac6175305455424497ea34c91ba91c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:42 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:42 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:42 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:31:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
USER kong
# Thu, 15 Jan 2026 22:31:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:31:08 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:31:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:31:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0e71ec567dafc82f9a26f33506f67e23ba294e4dbe6b27de73bd88392a7e9`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95851f6441bbd0f5f9788340df95d53e219766679056619f090aa9a8c903e79`  
		Last Modified: Thu, 15 Jan 2026 22:31:22 GMT  
		Size: 62.7 MB (62740022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dede8248c1ebec209468671cd27f767862068057ebb706b9b7b73792bc5b29c5`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:d0d9ee5d35e3cd8ee5c3ccc5eeb8af273924bc92790c29358989b8ee2f2f64b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0d50d27d9f9e85adfbce006960ee4b6b0ec8e7dfff8a6d2bb633878178de`

```dockerfile
```

-	Layers:
	-	`sha256:b08f90a940ccf492c4bf8c9846504c4ccfaf8b6c3f2a1a16342b1e2f2340ca9e`  
		Last Modified: Thu, 15 Jan 2026 22:31:21 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:956db8aa9b642e8da3eb504c20472c0ca75334a86790cf425411616c438c69dd`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d5c3cf7171aed6ff0a6f82bc5069230942601a0bfd97684dfdfdde2e82ec8eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88583046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba5e14fea720da46c9d92e28922fdcc8871396caa188cbb43172309c7094e35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:52 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:33:17 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
USER kong
# Thu, 15 Jan 2026 22:33:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:17 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf70b612faec25c975e123e76f8846cb269cef9ad4b043a14c3afcc351232c`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514eb4e0ecc2bec3f614b60fa1fbb69f7ded6fb801a3b63ca5187f92495351f7`  
		Last Modified: Thu, 15 Jan 2026 22:33:33 GMT  
		Size: 61.2 MB (61198266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb647d3e5367c87e2202482e6815abaebbf63639e9bf90d841f4b9aef5bd0be`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:c8dd415c6c9253d1c7fcc93808679889183fdbade251c6816887591c8ec80fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8110f2a5a233d1b99b5e95a80bbace9615ce1e32f85a02583c0aa1bfd01c328d`

```dockerfile
```

-	Layers:
	-	`sha256:ad10c7eafd53f3768dd2abb1521a04edef6fb8de1ebbb1dbb6f174747d86dc44`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3802f104f039261cbb60e96645222259ad4b3dd713655594856a73e99a3d0051`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:006359bd9a1625dbebad43fda751bb9851b394686bfc8cee6e9d93b041263ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ea07d14bfbba3adc5337e93f9532022fe164ce5cf493dfcdf749d8d38d4c5683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92277971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f5aba4c1f2dc2e6089308119adfd64ac6175305455424497ea34c91ba91c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:42 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:42 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:42 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:42 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:30:42 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:31:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:08 GMT
USER kong
# Thu, 15 Jan 2026 22:31:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:31:08 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:31:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:31:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0e71ec567dafc82f9a26f33506f67e23ba294e4dbe6b27de73bd88392a7e9`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95851f6441bbd0f5f9788340df95d53e219766679056619f090aa9a8c903e79`  
		Last Modified: Thu, 15 Jan 2026 22:31:22 GMT  
		Size: 62.7 MB (62740022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dede8248c1ebec209468671cd27f767862068057ebb706b9b7b73792bc5b29c5`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d0d9ee5d35e3cd8ee5c3ccc5eeb8af273924bc92790c29358989b8ee2f2f64b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0d50d27d9f9e85adfbce006960ee4b6b0ec8e7dfff8a6d2bb633878178de`

```dockerfile
```

-	Layers:
	-	`sha256:b08f90a940ccf492c4bf8c9846504c4ccfaf8b6c3f2a1a16342b1e2f2340ca9e`  
		Last Modified: Thu, 15 Jan 2026 22:31:21 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:956db8aa9b642e8da3eb504c20472c0ca75334a86790cf425411616c438c69dd`  
		Last Modified: Thu, 15 Jan 2026 22:31:20 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d5c3cf7171aed6ff0a6f82bc5069230942601a0bfd97684dfdfdde2e82ec8eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88583046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba5e14fea720da46c9d92e28922fdcc8871396caa188cbb43172309c7094e35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:52 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:52 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ENV KONG_VERSION=3.4.2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 15 Jan 2026 22:32:52 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 15 Jan 2026 22:33:17 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:17 GMT
USER kong
# Thu, 15 Jan 2026 22:33:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:17 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf70b612faec25c975e123e76f8846cb269cef9ad4b043a14c3afcc351232c`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514eb4e0ecc2bec3f614b60fa1fbb69f7ded6fb801a3b63ca5187f92495351f7`  
		Last Modified: Thu, 15 Jan 2026 22:33:33 GMT  
		Size: 61.2 MB (61198266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb647d3e5367c87e2202482e6815abaebbf63639e9bf90d841f4b9aef5bd0be`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c8dd415c6c9253d1c7fcc93808679889183fdbade251c6816887591c8ec80fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8110f2a5a233d1b99b5e95a80bbace9615ce1e32f85a02583c0aa1bfd01c328d`

```dockerfile
```

-	Layers:
	-	`sha256:ad10c7eafd53f3768dd2abb1521a04edef6fb8de1ebbb1dbb6f174747d86dc44`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3802f104f039261cbb60e96645222259ad4b3dd713655594856a73e99a3d0051`  
		Last Modified: Thu, 15 Jan 2026 22:33:31 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:472220b49589080d7b39956efe8ff12e3a6ed66336726c099c230b38913376d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:c959f4b328bb7e4145e5a57a62ea21b127c85db8175ede8ceea9f29160fed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117548004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c10993f1b9c6686d675d316aa464ea131e60f12dfd951b13f5d8c5925807551`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:29 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:30:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
USER kong
# Thu, 15 Jan 2026 22:30:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f23990583303fc944ebfc7f46c5a8bc5de37c183284b95481159058b76fee3`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62153f526fc71913161675a50fbc640c68433beca916760bad7065c5aee113`  
		Last Modified: Thu, 15 Jan 2026 22:31:14 GMT  
		Size: 88.0 MB (88010050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991d904b3a9f6e49805dff4c31bf19809ccf76e459b07e35a84e80c63bb478b`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:62b8e24f11c1ada6a92ba32dc1d72b0a0c8e8e6f2a0b72957ccb0c67e2256118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ec31b4ee1dee068410407aec980276ce5f02bf41de1295430c91360f603eb8`

```dockerfile
```

-	Layers:
	-	`sha256:7e2319dd05709f386f4ab875e37f26b870a9a07bad447db29b149ae1c8a2129f`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c2cba837879fdc4dfa45245bfd981958b20bc2f3d9be666eee7b257eca0065`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a20781b3e2dde158c984a6e0bbd7ab833f055cd184d4e464d75d86a92e98bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbb0d268e021898186932d2ab71bd6f39a4eb1017e06a483b51badfc974638d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:37 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:37 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:37 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:33:02 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
USER kong
# Thu, 15 Jan 2026 22:33:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:02 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c849fb03a7a5e9b32fe20fd8be20382ecd63b63c2d7029b1ae4f716abe2d63b`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac65f2a6da6984e8fda10316819ae7502b92d87f2cdaaa6572d5ccae5229be`  
		Last Modified: Thu, 15 Jan 2026 22:33:21 GMT  
		Size: 87.3 MB (87288939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7576e1a204f037eba8322e5acc461a8e7deba571da5d45a5dedce1c0f2b1fc`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:f2a34ce16f993dde4a438cc2eb9e6590caaf052ae9229e3f3f36942f8e70eea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d142c3331ccfce317a71170b3d3f0bc41b9bed9b04663bcd22b0524e09a6e4`

```dockerfile
```

-	Layers:
	-	`sha256:4f42707d0a4d9e721f4b4baf60110fec506dd3a3f7c7491e18245b143e955d57`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7051baa12ffa432de7543345a7f9fd0b245e75aff86b25212c3b0970d2ae59`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:472220b49589080d7b39956efe8ff12e3a6ed66336726c099c230b38913376d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c959f4b328bb7e4145e5a57a62ea21b127c85db8175ede8ceea9f29160fed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117548004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c10993f1b9c6686d675d316aa464ea131e60f12dfd951b13f5d8c5925807551`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:29 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:30:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
USER kong
# Thu, 15 Jan 2026 22:30:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f23990583303fc944ebfc7f46c5a8bc5de37c183284b95481159058b76fee3`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62153f526fc71913161675a50fbc640c68433beca916760bad7065c5aee113`  
		Last Modified: Thu, 15 Jan 2026 22:31:14 GMT  
		Size: 88.0 MB (88010050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991d904b3a9f6e49805dff4c31bf19809ccf76e459b07e35a84e80c63bb478b`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:62b8e24f11c1ada6a92ba32dc1d72b0a0c8e8e6f2a0b72957ccb0c67e2256118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ec31b4ee1dee068410407aec980276ce5f02bf41de1295430c91360f603eb8`

```dockerfile
```

-	Layers:
	-	`sha256:7e2319dd05709f386f4ab875e37f26b870a9a07bad447db29b149ae1c8a2129f`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c2cba837879fdc4dfa45245bfd981958b20bc2f3d9be666eee7b257eca0065`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a20781b3e2dde158c984a6e0bbd7ab833f055cd184d4e464d75d86a92e98bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbb0d268e021898186932d2ab71bd6f39a4eb1017e06a483b51badfc974638d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:37 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:37 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:37 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:33:02 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
USER kong
# Thu, 15 Jan 2026 22:33:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:02 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c849fb03a7a5e9b32fe20fd8be20382ecd63b63c2d7029b1ae4f716abe2d63b`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac65f2a6da6984e8fda10316819ae7502b92d87f2cdaaa6572d5ccae5229be`  
		Last Modified: Thu, 15 Jan 2026 22:33:21 GMT  
		Size: 87.3 MB (87288939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7576e1a204f037eba8322e5acc461a8e7deba571da5d45a5dedce1c0f2b1fc`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f2a34ce16f993dde4a438cc2eb9e6590caaf052ae9229e3f3f36942f8e70eea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d142c3331ccfce317a71170b3d3f0bc41b9bed9b04663bcd22b0524e09a6e4`

```dockerfile
```

-	Layers:
	-	`sha256:4f42707d0a4d9e721f4b4baf60110fec506dd3a3f7c7491e18245b143e955d57`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7051baa12ffa432de7543345a7f9fd0b245e75aff86b25212c3b0970d2ae59`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:472220b49589080d7b39956efe8ff12e3a6ed66336726c099c230b38913376d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:c959f4b328bb7e4145e5a57a62ea21b127c85db8175ede8ceea9f29160fed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117548004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c10993f1b9c6686d675d316aa464ea131e60f12dfd951b13f5d8c5925807551`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:29 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:30:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
USER kong
# Thu, 15 Jan 2026 22:30:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f23990583303fc944ebfc7f46c5a8bc5de37c183284b95481159058b76fee3`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62153f526fc71913161675a50fbc640c68433beca916760bad7065c5aee113`  
		Last Modified: Thu, 15 Jan 2026 22:31:14 GMT  
		Size: 88.0 MB (88010050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991d904b3a9f6e49805dff4c31bf19809ccf76e459b07e35a84e80c63bb478b`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:62b8e24f11c1ada6a92ba32dc1d72b0a0c8e8e6f2a0b72957ccb0c67e2256118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ec31b4ee1dee068410407aec980276ce5f02bf41de1295430c91360f603eb8`

```dockerfile
```

-	Layers:
	-	`sha256:7e2319dd05709f386f4ab875e37f26b870a9a07bad447db29b149ae1c8a2129f`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c2cba837879fdc4dfa45245bfd981958b20bc2f3d9be666eee7b257eca0065`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a20781b3e2dde158c984a6e0bbd7ab833f055cd184d4e464d75d86a92e98bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbb0d268e021898186932d2ab71bd6f39a4eb1017e06a483b51badfc974638d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:37 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:37 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:37 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:33:02 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
USER kong
# Thu, 15 Jan 2026 22:33:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:02 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c849fb03a7a5e9b32fe20fd8be20382ecd63b63c2d7029b1ae4f716abe2d63b`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac65f2a6da6984e8fda10316819ae7502b92d87f2cdaaa6572d5ccae5229be`  
		Last Modified: Thu, 15 Jan 2026 22:33:21 GMT  
		Size: 87.3 MB (87288939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7576e1a204f037eba8322e5acc461a8e7deba571da5d45a5dedce1c0f2b1fc`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:f2a34ce16f993dde4a438cc2eb9e6590caaf052ae9229e3f3f36942f8e70eea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d142c3331ccfce317a71170b3d3f0bc41b9bed9b04663bcd22b0524e09a6e4`

```dockerfile
```

-	Layers:
	-	`sha256:4f42707d0a4d9e721f4b4baf60110fec506dd3a3f7c7491e18245b143e955d57`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7051baa12ffa432de7543345a7f9fd0b245e75aff86b25212c3b0970d2ae59`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:472220b49589080d7b39956efe8ff12e3a6ed66336726c099c230b38913376d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c959f4b328bb7e4145e5a57a62ea21b127c85db8175ede8ceea9f29160fed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117548004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c10993f1b9c6686d675d316aa464ea131e60f12dfd951b13f5d8c5925807551`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:29 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:29 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:30:29 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:30:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:56 GMT
USER kong
# Thu, 15 Jan 2026 22:30:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f23990583303fc944ebfc7f46c5a8bc5de37c183284b95481159058b76fee3`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62153f526fc71913161675a50fbc640c68433beca916760bad7065c5aee113`  
		Last Modified: Thu, 15 Jan 2026 22:31:14 GMT  
		Size: 88.0 MB (88010050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991d904b3a9f6e49805dff4c31bf19809ccf76e459b07e35a84e80c63bb478b`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:62b8e24f11c1ada6a92ba32dc1d72b0a0c8e8e6f2a0b72957ccb0c67e2256118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ec31b4ee1dee068410407aec980276ce5f02bf41de1295430c91360f603eb8`

```dockerfile
```

-	Layers:
	-	`sha256:7e2319dd05709f386f4ab875e37f26b870a9a07bad447db29b149ae1c8a2129f`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c2cba837879fdc4dfa45245bfd981958b20bc2f3d9be666eee7b257eca0065`  
		Last Modified: Thu, 15 Jan 2026 22:31:12 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a20781b3e2dde158c984a6e0bbd7ab833f055cd184d4e464d75d86a92e98bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbb0d268e021898186932d2ab71bd6f39a4eb1017e06a483b51badfc974638d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:37 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:37 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:37 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:37 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ENV KONG_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 15 Jan 2026 22:32:37 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 15 Jan 2026 22:33:02 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:33:02 GMT
USER kong
# Thu, 15 Jan 2026 22:33:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:33:02 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:33:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:33:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:33:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c849fb03a7a5e9b32fe20fd8be20382ecd63b63c2d7029b1ae4f716abe2d63b`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac65f2a6da6984e8fda10316819ae7502b92d87f2cdaaa6572d5ccae5229be`  
		Last Modified: Thu, 15 Jan 2026 22:33:21 GMT  
		Size: 87.3 MB (87288939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7576e1a204f037eba8322e5acc461a8e7deba571da5d45a5dedce1c0f2b1fc`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f2a34ce16f993dde4a438cc2eb9e6590caaf052ae9229e3f3f36942f8e70eea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d142c3331ccfce317a71170b3d3f0bc41b9bed9b04663bcd22b0524e09a6e4`

```dockerfile
```

-	Layers:
	-	`sha256:4f42707d0a4d9e721f4b4baf60110fec506dd3a3f7c7491e18245b143e955d57`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7051baa12ffa432de7543345a7f9fd0b245e75aff86b25212c3b0970d2ae59`  
		Last Modified: Thu, 15 Jan 2026 22:33:19 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:9111d452bf4092245edd8b567d54c68f98c71d1a41eb0db84a2cb356af22da93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:2764b27f1f117d51e330d50f61db52d3800e650c2cfde0c0f94e15c06d3bf856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120411808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c4dd0ea26887a49e56fa59bd9569279239e7206ef03b0dfad5709310623ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:17 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:17 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:30:45 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
USER kong
# Thu, 15 Jan 2026 22:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:45 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb43f2c090f9362734ce2de3a4a83bb30decf80c1443d1847df95b79b1f6d9fc`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf064bb91096baef29f3dbf0b58457237673ed8809e734c26f03980d1d2cb1ab`  
		Last Modified: Thu, 15 Jan 2026 22:31:04 GMT  
		Size: 90.7 MB (90684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d53bd57a1e4c36ec63b892de6040a2a2ad99a810641f4ae3b14f30229281`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:77f2eca4db4c0d23f05356f9c9e05355c90d92d831e56b138a2115ea256dda15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f535ff2014658e105b80acdffbb397d09abe247f35020a13c586ad0e3f52c76`

```dockerfile
```

-	Layers:
	-	`sha256:318437fe8f73cce9afab408b58ca0c322060b5cb9c940e8797c88280140dc18a`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d05dadb7fb79dc281703a043b2b774da3f5a4a636337bd4220baa894b9eb79`  
		Last Modified: Thu, 15 Jan 2026 22:31:01 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9e558058ac6169e0a47ce01365ccbb5ae38fdf97be810582747e007ae96c81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118867702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c546477b1dd5cfeab175e87a6f81fab2b9e764a1d84e9c2931bcffbc27b6517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:21 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:32:50 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
USER kong
# Thu, 15 Jan 2026 22:32:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:50 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:32:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:32:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:32:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304f900a467aa61e07e6f11db6758e7a4c4c1c6da6979d0db9689e5bf73e059`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21bd5760326a990eda6c683d407beba3e5d32c5af5cfc912dcf108acdb864b2`  
		Last Modified: Thu, 15 Jan 2026 22:33:09 GMT  
		Size: 90.0 MB (90002592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbad4a31f221f9459047227092b06d9d87a6eb164d0d10f0f583116f715ae20`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:c4f0fd068c5196bc29d65a6b59407891306beec7604a3ed164900ad8188fbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac98a8bd40e76c88e79cd49c5e154c0d97aae550f25125d7238c8f79c91370d`

```dockerfile
```

-	Layers:
	-	`sha256:2e22ca6e0f57a5d72f509b43d1ddfe2be5bcd344b6a5df1af5b74af9db5a725c`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37823ba562e181ffb17b2465123b3f2c2579e4cfc3144b3c481c63397bcd76c2`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:9111d452bf4092245edd8b567d54c68f98c71d1a41eb0db84a2cb356af22da93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2764b27f1f117d51e330d50f61db52d3800e650c2cfde0c0f94e15c06d3bf856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120411808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c4dd0ea26887a49e56fa59bd9569279239e7206ef03b0dfad5709310623ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:17 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:17 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:30:45 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
USER kong
# Thu, 15 Jan 2026 22:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:45 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb43f2c090f9362734ce2de3a4a83bb30decf80c1443d1847df95b79b1f6d9fc`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf064bb91096baef29f3dbf0b58457237673ed8809e734c26f03980d1d2cb1ab`  
		Last Modified: Thu, 15 Jan 2026 22:31:04 GMT  
		Size: 90.7 MB (90684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d53bd57a1e4c36ec63b892de6040a2a2ad99a810641f4ae3b14f30229281`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:77f2eca4db4c0d23f05356f9c9e05355c90d92d831e56b138a2115ea256dda15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f535ff2014658e105b80acdffbb397d09abe247f35020a13c586ad0e3f52c76`

```dockerfile
```

-	Layers:
	-	`sha256:318437fe8f73cce9afab408b58ca0c322060b5cb9c940e8797c88280140dc18a`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d05dadb7fb79dc281703a043b2b774da3f5a4a636337bd4220baa894b9eb79`  
		Last Modified: Thu, 15 Jan 2026 22:31:01 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9e558058ac6169e0a47ce01365ccbb5ae38fdf97be810582747e007ae96c81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118867702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c546477b1dd5cfeab175e87a6f81fab2b9e764a1d84e9c2931bcffbc27b6517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:21 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:32:50 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
USER kong
# Thu, 15 Jan 2026 22:32:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:50 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:32:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:32:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:32:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304f900a467aa61e07e6f11db6758e7a4c4c1c6da6979d0db9689e5bf73e059`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21bd5760326a990eda6c683d407beba3e5d32c5af5cfc912dcf108acdb864b2`  
		Last Modified: Thu, 15 Jan 2026 22:33:09 GMT  
		Size: 90.0 MB (90002592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbad4a31f221f9459047227092b06d9d87a6eb164d0d10f0f583116f715ae20`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c4f0fd068c5196bc29d65a6b59407891306beec7604a3ed164900ad8188fbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac98a8bd40e76c88e79cd49c5e154c0d97aae550f25125d7238c8f79c91370d`

```dockerfile
```

-	Layers:
	-	`sha256:2e22ca6e0f57a5d72f509b43d1ddfe2be5bcd344b6a5df1af5b74af9db5a725c`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37823ba562e181ffb17b2465123b3f2c2579e4cfc3144b3c481c63397bcd76c2`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:9111d452bf4092245edd8b567d54c68f98c71d1a41eb0db84a2cb356af22da93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:2764b27f1f117d51e330d50f61db52d3800e650c2cfde0c0f94e15c06d3bf856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120411808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c4dd0ea26887a49e56fa59bd9569279239e7206ef03b0dfad5709310623ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:17 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:17 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:30:45 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
USER kong
# Thu, 15 Jan 2026 22:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:45 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb43f2c090f9362734ce2de3a4a83bb30decf80c1443d1847df95b79b1f6d9fc`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf064bb91096baef29f3dbf0b58457237673ed8809e734c26f03980d1d2cb1ab`  
		Last Modified: Thu, 15 Jan 2026 22:31:04 GMT  
		Size: 90.7 MB (90684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d53bd57a1e4c36ec63b892de6040a2a2ad99a810641f4ae3b14f30229281`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:77f2eca4db4c0d23f05356f9c9e05355c90d92d831e56b138a2115ea256dda15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f535ff2014658e105b80acdffbb397d09abe247f35020a13c586ad0e3f52c76`

```dockerfile
```

-	Layers:
	-	`sha256:318437fe8f73cce9afab408b58ca0c322060b5cb9c940e8797c88280140dc18a`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d05dadb7fb79dc281703a043b2b774da3f5a4a636337bd4220baa894b9eb79`  
		Last Modified: Thu, 15 Jan 2026 22:31:01 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9e558058ac6169e0a47ce01365ccbb5ae38fdf97be810582747e007ae96c81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118867702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c546477b1dd5cfeab175e87a6f81fab2b9e764a1d84e9c2931bcffbc27b6517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:21 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:32:50 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
USER kong
# Thu, 15 Jan 2026 22:32:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:50 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:32:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:32:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:32:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304f900a467aa61e07e6f11db6758e7a4c4c1c6da6979d0db9689e5bf73e059`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21bd5760326a990eda6c683d407beba3e5d32c5af5cfc912dcf108acdb864b2`  
		Last Modified: Thu, 15 Jan 2026 22:33:09 GMT  
		Size: 90.0 MB (90002592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbad4a31f221f9459047227092b06d9d87a6eb164d0d10f0f583116f715ae20`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:c4f0fd068c5196bc29d65a6b59407891306beec7604a3ed164900ad8188fbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac98a8bd40e76c88e79cd49c5e154c0d97aae550f25125d7238c8f79c91370d`

```dockerfile
```

-	Layers:
	-	`sha256:2e22ca6e0f57a5d72f509b43d1ddfe2be5bcd344b6a5df1af5b74af9db5a725c`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37823ba562e181ffb17b2465123b3f2c2579e4cfc3144b3c481c63397bcd76c2`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:9111d452bf4092245edd8b567d54c68f98c71d1a41eb0db84a2cb356af22da93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2764b27f1f117d51e330d50f61db52d3800e650c2cfde0c0f94e15c06d3bf856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120411808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c4dd0ea26887a49e56fa59bd9569279239e7206ef03b0dfad5709310623ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:17 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:17 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:30:45 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
USER kong
# Thu, 15 Jan 2026 22:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:45 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb43f2c090f9362734ce2de3a4a83bb30decf80c1443d1847df95b79b1f6d9fc`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf064bb91096baef29f3dbf0b58457237673ed8809e734c26f03980d1d2cb1ab`  
		Last Modified: Thu, 15 Jan 2026 22:31:04 GMT  
		Size: 90.7 MB (90684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d53bd57a1e4c36ec63b892de6040a2a2ad99a810641f4ae3b14f30229281`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:77f2eca4db4c0d23f05356f9c9e05355c90d92d831e56b138a2115ea256dda15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f535ff2014658e105b80acdffbb397d09abe247f35020a13c586ad0e3f52c76`

```dockerfile
```

-	Layers:
	-	`sha256:318437fe8f73cce9afab408b58ca0c322060b5cb9c940e8797c88280140dc18a`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d05dadb7fb79dc281703a043b2b774da3f5a4a636337bd4220baa894b9eb79`  
		Last Modified: Thu, 15 Jan 2026 22:31:01 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9e558058ac6169e0a47ce01365ccbb5ae38fdf97be810582747e007ae96c81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118867702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c546477b1dd5cfeab175e87a6f81fab2b9e764a1d84e9c2931bcffbc27b6517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:21 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:32:50 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
USER kong
# Thu, 15 Jan 2026 22:32:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:50 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:32:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:32:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:32:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304f900a467aa61e07e6f11db6758e7a4c4c1c6da6979d0db9689e5bf73e059`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21bd5760326a990eda6c683d407beba3e5d32c5af5cfc912dcf108acdb864b2`  
		Last Modified: Thu, 15 Jan 2026 22:33:09 GMT  
		Size: 90.0 MB (90002592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbad4a31f221f9459047227092b06d9d87a6eb164d0d10f0f583116f715ae20`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c4f0fd068c5196bc29d65a6b59407891306beec7604a3ed164900ad8188fbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac98a8bd40e76c88e79cd49c5e154c0d97aae550f25125d7238c8f79c91370d`

```dockerfile
```

-	Layers:
	-	`sha256:2e22ca6e0f57a5d72f509b43d1ddfe2be5bcd344b6a5df1af5b74af9db5a725c`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37823ba562e181ffb17b2465123b3f2c2579e4cfc3144b3c481c63397bcd76c2`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:9111d452bf4092245edd8b567d54c68f98c71d1a41eb0db84a2cb356af22da93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:2764b27f1f117d51e330d50f61db52d3800e650c2cfde0c0f94e15c06d3bf856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120411808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c4dd0ea26887a49e56fa59bd9569279239e7206ef03b0dfad5709310623ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:17 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:17 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:30:45 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
USER kong
# Thu, 15 Jan 2026 22:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:45 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb43f2c090f9362734ce2de3a4a83bb30decf80c1443d1847df95b79b1f6d9fc`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf064bb91096baef29f3dbf0b58457237673ed8809e734c26f03980d1d2cb1ab`  
		Last Modified: Thu, 15 Jan 2026 22:31:04 GMT  
		Size: 90.7 MB (90684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d53bd57a1e4c36ec63b892de6040a2a2ad99a810641f4ae3b14f30229281`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:77f2eca4db4c0d23f05356f9c9e05355c90d92d831e56b138a2115ea256dda15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f535ff2014658e105b80acdffbb397d09abe247f35020a13c586ad0e3f52c76`

```dockerfile
```

-	Layers:
	-	`sha256:318437fe8f73cce9afab408b58ca0c322060b5cb9c940e8797c88280140dc18a`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d05dadb7fb79dc281703a043b2b774da3f5a4a636337bd4220baa894b9eb79`  
		Last Modified: Thu, 15 Jan 2026 22:31:01 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9e558058ac6169e0a47ce01365ccbb5ae38fdf97be810582747e007ae96c81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118867702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c546477b1dd5cfeab175e87a6f81fab2b9e764a1d84e9c2931bcffbc27b6517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:21 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:32:50 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
USER kong
# Thu, 15 Jan 2026 22:32:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:50 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:32:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:32:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:32:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304f900a467aa61e07e6f11db6758e7a4c4c1c6da6979d0db9689e5bf73e059`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21bd5760326a990eda6c683d407beba3e5d32c5af5cfc912dcf108acdb864b2`  
		Last Modified: Thu, 15 Jan 2026 22:33:09 GMT  
		Size: 90.0 MB (90002592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbad4a31f221f9459047227092b06d9d87a6eb164d0d10f0f583116f715ae20`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:c4f0fd068c5196bc29d65a6b59407891306beec7604a3ed164900ad8188fbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac98a8bd40e76c88e79cd49c5e154c0d97aae550f25125d7238c8f79c91370d`

```dockerfile
```

-	Layers:
	-	`sha256:2e22ca6e0f57a5d72f509b43d1ddfe2be5bcd344b6a5df1af5b74af9db5a725c`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37823ba562e181ffb17b2465123b3f2c2579e4cfc3144b3c481c63397bcd76c2`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:9111d452bf4092245edd8b567d54c68f98c71d1a41eb0db84a2cb356af22da93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2764b27f1f117d51e330d50f61db52d3800e650c2cfde0c0f94e15c06d3bf856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120411808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c4dd0ea26887a49e56fa59bd9569279239e7206ef03b0dfad5709310623ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:30:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:30:17 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:30:17 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:30:17 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:30:17 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:30:45 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:30:45 GMT
USER kong
# Thu, 15 Jan 2026 22:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:30:45 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:30:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:30:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:30:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb43f2c090f9362734ce2de3a4a83bb30decf80c1443d1847df95b79b1f6d9fc`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf064bb91096baef29f3dbf0b58457237673ed8809e734c26f03980d1d2cb1ab`  
		Last Modified: Thu, 15 Jan 2026 22:31:04 GMT  
		Size: 90.7 MB (90684511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9d53bd57a1e4c36ec63b892de6040a2a2ad99a810641f4ae3b14f30229281`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:77f2eca4db4c0d23f05356f9c9e05355c90d92d831e56b138a2115ea256dda15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f535ff2014658e105b80acdffbb397d09abe247f35020a13c586ad0e3f52c76`

```dockerfile
```

-	Layers:
	-	`sha256:318437fe8f73cce9afab408b58ca0c322060b5cb9c940e8797c88280140dc18a`  
		Last Modified: Thu, 15 Jan 2026 22:31:02 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d05dadb7fb79dc281703a043b2b774da3f5a4a636337bd4220baa894b9eb79`  
		Last Modified: Thu, 15 Jan 2026 22:31:01 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9e558058ac6169e0a47ce01365ccbb5ae38fdf97be810582747e007ae96c81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118867702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c546477b1dd5cfeab175e87a6f81fab2b9e764a1d84e9c2931bcffbc27b6517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

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
# Thu, 15 Jan 2026 22:32:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 15 Jan 2026 22:32:21 GMT
ARG ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ENV ASSET=ce
# Thu, 15 Jan 2026 22:32:21 GMT
ARG EE_PORTS
# Thu, 15 Jan 2026 22:32:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ENV KONG_VERSION=3.9.1
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 15 Jan 2026 22:32:21 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 15 Jan 2026 22:32:50 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:50 GMT
USER kong
# Thu, 15 Jan 2026 22:32:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:50 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 15 Jan 2026 22:32:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:32:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 15 Jan 2026 22:32:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c304f900a467aa61e07e6f11db6758e7a4c4c1c6da6979d0db9689e5bf73e059`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21bd5760326a990eda6c683d407beba3e5d32c5af5cfc912dcf108acdb864b2`  
		Last Modified: Thu, 15 Jan 2026 22:33:09 GMT  
		Size: 90.0 MB (90002592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbad4a31f221f9459047227092b06d9d87a6eb164d0d10f0f583116f715ae20`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c4f0fd068c5196bc29d65a6b59407891306beec7604a3ed164900ad8188fbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac98a8bd40e76c88e79cd49c5e154c0d97aae550f25125d7238c8f79c91370d`

```dockerfile
```

-	Layers:
	-	`sha256:2e22ca6e0f57a5d72f509b43d1ddfe2be5bcd344b6a5df1af5b74af9db5a725c`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37823ba562e181ffb17b2465123b3f2c2579e4cfc3144b3c481c63397bcd76c2`  
		Last Modified: Thu, 15 Jan 2026 22:33:07 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json
