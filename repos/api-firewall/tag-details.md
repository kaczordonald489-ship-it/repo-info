<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.9.5`](#api-firewall095)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.9.5`

```console
$ docker pull api-firewall@sha256:423c921768a43f4eb23779c8b7cdd7e7758776c3950ac916fff50c894d230b9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:0.9.5` - linux; amd64

```console
$ docker pull api-firewall@sha256:e4a11975d3bd48b77652800bf17460f5ebdeabf9623fc7c7501b0846ebf28bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17401569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c3e974eaf8157885c4e42261001a9d0662282ebe2fd6d27365cff9220e2907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:13:58 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 28 Jan 2026 02:13:58 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:13:58 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 28 Jan 2026 02:13:58 GMT
ENV APIFIREWALL_VERSION=v0.9.5
# Wed, 28 Jan 2026 02:14:00 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='945145404a43dc1e353402aa9d9a6000e31e8222c769c70141873de61a6293c3';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='8b977a5a9ebc9152d64fb3bc3dc5afa9f317fd65244b0a49249805b6632caba3';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ebdff4996617a5f9b54010b4cfe084cd0c061e0e119d12fc198498f495bbc6f7';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 28 Jan 2026 02:14:00 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 28 Jan 2026 02:14:00 GMT
USER api-firewall
# Wed, 28 Jan 2026 02:14:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:00 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e09137debb8c7614df0703a231d01bff1a229b9e46cde804f96aac22288e93`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e18e5bf716499cd711c851152bd47bb289867155ccf48ab0789ef5c7e4c2c`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 13.6 MB (13595440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b0a96e26078f9684bbbc5ff8877d28f5f4edb413b1b2431dc8d68a8a67912e`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.5` - unknown; unknown

```console
$ docker pull api-firewall@sha256:d541594ad6e87217e52c94a2830619bd1d94d549b97b3d8a82a4499f30ec105e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3139b2d4773d267a524be8610994d986486989f37121434f40a1061a2dfc6a4`

```dockerfile
```

-	Layers:
	-	`sha256:bdedd73534bed2a9b7d2ef19699ce9309934801174da2b6a2dc1c844f30b7d73`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 167.0 KB (166989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45217994128db9cd707ebc98271a6a86b0f7d4049e75039807f0535480975a78`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 13.5 KB (13503 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.5` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:493ad0f456c6b197bc58b3c7cc38d8757fea6fa6935619bec8476e9ed11a2fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16650818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f82d5483ff5d73e470423b6132631497c9a8ff39879a83718096522b6ac35b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:14:46 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 28 Jan 2026 02:14:46 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:14:46 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 28 Jan 2026 02:14:46 GMT
ENV APIFIREWALL_VERSION=v0.9.5
# Wed, 28 Jan 2026 02:14:48 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='945145404a43dc1e353402aa9d9a6000e31e8222c769c70141873de61a6293c3';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='8b977a5a9ebc9152d64fb3bc3dc5afa9f317fd65244b0a49249805b6632caba3';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ebdff4996617a5f9b54010b4cfe084cd0c061e0e119d12fc198498f495bbc6f7';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 28 Jan 2026 02:14:48 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 28 Jan 2026 02:14:48 GMT
USER api-firewall
# Wed, 28 Jan 2026 02:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:48 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb774da3aa936e3ef2e71f9d8d8b099e09894d6e59d2b29b73f5ae3bd0ec3d0`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a207111ce8d4acef591aa104c04453f64a4c39be6480b43d255addb794295f25`  
		Last Modified: Wed, 28 Jan 2026 02:14:54 GMT  
		Size: 12.5 MB (12510046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beabc5e9f298484a3b74a0aaf1aeaaad2bee39afb22c3fe0f4b5063d4ef2ea94`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.5` - unknown; unknown

```console
$ docker pull api-firewall@sha256:47ef6571e835d41ac07a35e8f4213533060c525b33a5007a9abea01a394c1002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 KB (180619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0501e15303603f904f045154204c16cec732d92119d5ee0eb28d6314e4d7e814`

```dockerfile
```

-	Layers:
	-	`sha256:52548306cb27204a599dbe32d0de75fb0aa34c5b144e437df0f0d0bf67b22010`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 167.0 KB (167021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e05b8206b7c08f807b5daf39401db4722e3ea1bbf38d013bb2fcdd517d36cad`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 13.6 KB (13598 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.5` - linux; 386

```console
$ docker pull api-firewall@sha256:7e870093025c0305241f94456f8fc5c518a57202f00c3337a8d29000a3747305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f30eff9476b55edbac6a557eebb75c805869cffb167a416267814ec0c13405`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:14:19 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 28 Jan 2026 02:14:19 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:14:19 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 28 Jan 2026 02:14:19 GMT
ENV APIFIREWALL_VERSION=v0.9.5
# Wed, 28 Jan 2026 02:14:20 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='945145404a43dc1e353402aa9d9a6000e31e8222c769c70141873de61a6293c3';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='8b977a5a9ebc9152d64fb3bc3dc5afa9f317fd65244b0a49249805b6632caba3';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ebdff4996617a5f9b54010b4cfe084cd0c061e0e119d12fc198498f495bbc6f7';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 28 Jan 2026 02:14:20 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 28 Jan 2026 02:14:20 GMT
USER api-firewall
# Wed, 28 Jan 2026 02:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:20 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d686cf5b5b28b771ffe32590baa152b1a0fcffbfdac9f3f9dae11c3e5afd8d67`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6461d5605225fcd10bbd3df91250b2e4b372e64bd0a95adfccfa5c4dbbaf091e`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 12.1 MB (12057002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296a979750a7d5b4284e07d5b25d98b13b1b0770f4e66bf1f5f2c22d117b0bce`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.5` - unknown; unknown

```console
$ docker pull api-firewall@sha256:c7ae43c586394af16499d82d900a408dda354334be33a330be3fcfa634cee6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccfb150c52eedc32a91ed12a81590150e2c8cb66fd0c339d278cfac00ec616a`

```dockerfile
```

-	Layers:
	-	`sha256:84c31c57530ea618dca3ea9c2d6cf2e140ebe877fa3e9153696940e075d24dc3`  
		Last Modified: Wed, 28 Jan 2026 02:14:26 GMT  
		Size: 167.0 KB (166974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e87cb3dd2cab7e30909b8f25ab02e3c891262fd576df95aa610c870954c6d4`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 13.5 KB (13479 bytes)  
		MIME: application/vnd.in-toto+json

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:423c921768a43f4eb23779c8b7cdd7e7758776c3950ac916fff50c894d230b9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:e4a11975d3bd48b77652800bf17460f5ebdeabf9623fc7c7501b0846ebf28bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17401569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c3e974eaf8157885c4e42261001a9d0662282ebe2fd6d27365cff9220e2907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:13:58 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 28 Jan 2026 02:13:58 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:13:58 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 28 Jan 2026 02:13:58 GMT
ENV APIFIREWALL_VERSION=v0.9.5
# Wed, 28 Jan 2026 02:14:00 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='945145404a43dc1e353402aa9d9a6000e31e8222c769c70141873de61a6293c3';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='8b977a5a9ebc9152d64fb3bc3dc5afa9f317fd65244b0a49249805b6632caba3';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ebdff4996617a5f9b54010b4cfe084cd0c061e0e119d12fc198498f495bbc6f7';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 28 Jan 2026 02:14:00 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 28 Jan 2026 02:14:00 GMT
USER api-firewall
# Wed, 28 Jan 2026 02:14:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:00 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e09137debb8c7614df0703a231d01bff1a229b9e46cde804f96aac22288e93`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e18e5bf716499cd711c851152bd47bb289867155ccf48ab0789ef5c7e4c2c`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 13.6 MB (13595440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b0a96e26078f9684bbbc5ff8877d28f5f4edb413b1b2431dc8d68a8a67912e`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:d541594ad6e87217e52c94a2830619bd1d94d549b97b3d8a82a4499f30ec105e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3139b2d4773d267a524be8610994d986486989f37121434f40a1061a2dfc6a4`

```dockerfile
```

-	Layers:
	-	`sha256:bdedd73534bed2a9b7d2ef19699ce9309934801174da2b6a2dc1c844f30b7d73`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 167.0 KB (166989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45217994128db9cd707ebc98271a6a86b0f7d4049e75039807f0535480975a78`  
		Last Modified: Wed, 28 Jan 2026 02:14:06 GMT  
		Size: 13.5 KB (13503 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:493ad0f456c6b197bc58b3c7cc38d8757fea6fa6935619bec8476e9ed11a2fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16650818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f82d5483ff5d73e470423b6132631497c9a8ff39879a83718096522b6ac35b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:14:46 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 28 Jan 2026 02:14:46 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:14:46 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 28 Jan 2026 02:14:46 GMT
ENV APIFIREWALL_VERSION=v0.9.5
# Wed, 28 Jan 2026 02:14:48 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='945145404a43dc1e353402aa9d9a6000e31e8222c769c70141873de61a6293c3';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='8b977a5a9ebc9152d64fb3bc3dc5afa9f317fd65244b0a49249805b6632caba3';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ebdff4996617a5f9b54010b4cfe084cd0c061e0e119d12fc198498f495bbc6f7';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 28 Jan 2026 02:14:48 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 28 Jan 2026 02:14:48 GMT
USER api-firewall
# Wed, 28 Jan 2026 02:14:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:48 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb774da3aa936e3ef2e71f9d8d8b099e09894d6e59d2b29b73f5ae3bd0ec3d0`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a207111ce8d4acef591aa104c04453f64a4c39be6480b43d255addb794295f25`  
		Last Modified: Wed, 28 Jan 2026 02:14:54 GMT  
		Size: 12.5 MB (12510046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beabc5e9f298484a3b74a0aaf1aeaaad2bee39afb22c3fe0f4b5063d4ef2ea94`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:47ef6571e835d41ac07a35e8f4213533060c525b33a5007a9abea01a394c1002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 KB (180619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0501e15303603f904f045154204c16cec732d92119d5ee0eb28d6314e4d7e814`

```dockerfile
```

-	Layers:
	-	`sha256:52548306cb27204a599dbe32d0de75fb0aa34c5b144e437df0f0d0bf67b22010`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 167.0 KB (167021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e05b8206b7c08f807b5daf39401db4722e3ea1bbf38d013bb2fcdd517d36cad`  
		Last Modified: Wed, 28 Jan 2026 02:14:53 GMT  
		Size: 13.6 KB (13598 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:7e870093025c0305241f94456f8fc5c518a57202f00c3337a8d29000a3747305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f30eff9476b55edbac6a557eebb75c805869cffb167a416267814ec0c13405`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:14:19 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 28 Jan 2026 02:14:19 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:14:19 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 28 Jan 2026 02:14:19 GMT
ENV APIFIREWALL_VERSION=v0.9.5
# Wed, 28 Jan 2026 02:14:20 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='945145404a43dc1e353402aa9d9a6000e31e8222c769c70141873de61a6293c3';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='8b977a5a9ebc9152d64fb3bc3dc5afa9f317fd65244b0a49249805b6632caba3';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ebdff4996617a5f9b54010b4cfe084cd0c061e0e119d12fc198498f495bbc6f7';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 28 Jan 2026 02:14:20 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 28 Jan 2026 02:14:20 GMT
USER api-firewall
# Wed, 28 Jan 2026 02:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:20 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d686cf5b5b28b771ffe32590baa152b1a0fcffbfdac9f3f9dae11c3e5afd8d67`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6461d5605225fcd10bbd3df91250b2e4b372e64bd0a95adfccfa5c4dbbaf091e`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 12.1 MB (12057002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296a979750a7d5b4284e07d5b25d98b13b1b0770f4e66bf1f5f2c22d117b0bce`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:c7ae43c586394af16499d82d900a408dda354334be33a330be3fcfa634cee6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 KB (180453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccfb150c52eedc32a91ed12a81590150e2c8cb66fd0c339d278cfac00ec616a`

```dockerfile
```

-	Layers:
	-	`sha256:84c31c57530ea618dca3ea9c2d6cf2e140ebe877fa3e9153696940e075d24dc3`  
		Last Modified: Wed, 28 Jan 2026 02:14:26 GMT  
		Size: 167.0 KB (166974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e87cb3dd2cab7e30909b8f25ab02e3c891262fd576df95aa610c870954c6d4`  
		Last Modified: Wed, 28 Jan 2026 02:14:27 GMT  
		Size: 13.5 KB (13479 bytes)  
		MIME: application/vnd.in-toto+json
