<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:3`](#registry3)
-	[`registry:3.0`](#registry30)
-	[`registry:3.0.0`](#registry300)
-	[`registry:latest`](#registrylatest)

## `registry:3`

```console
$ docker pull registry@sha256:6c5666b861f3505b116bb9aa9b25175e71210414bd010d92035ff64018f9457e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3` - linux; amd64

```console
$ docker pull registry@sha256:5b12b22f21522fe69443079df04c0f3f42cb9977857f3c20404386652a6c6d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18549482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b916d8206bcbfc54c95fb06076751932c902254277f149b082dd5d4d67fccb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:36:15 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:36:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:15 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2f893a11eee550abbadc144efb3cccc151908f28f8a20775e6e990065d8b34`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 291.1 KB (291125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeded8eec5f8394cf132cd851680a68d0861eacaeb3dfdce2df957303cb5beb`  
		Last Modified: Wed, 28 Jan 2026 02:36:23 GMT  
		Size: 14.6 MB (14614005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8100d968019ced9a7dccd30207ff9e8781702aadbc3f409202021fb98aad4ef`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369e5bd3505f549f6bbad4856b935f10097b8cfb09774ca9064e510a9435ba0`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:c80f16a2e278a83f48c54afb114e4838086b2c88dce0924c0fbc4346cd9a694d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 KB (281083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2137385e84d71cfe37712458553b58efc2b14294c63c72c30fac3ee8936e00f8`

```dockerfile
```

-	Layers:
	-	`sha256:e7513cd118306c3b5d92385ed98fc5c801062e5d43ec34751fdcce10f5287e1e`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 266.8 KB (266799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db921fed581e221e8c8e3a194d71ead75542a129e98d77afa02dc58759fba749`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm variant v6

```console
$ docker pull registry@sha256:c2540c3e0f60b6f222233fe4f1c8c4f70ec75168bb2bcbaf901ec5c3408ff50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17382960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3acf3750b01ad98f470e0f16647a8765fe4abd2149b70dab4cbd11dc07f0ac7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:56:41 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:56:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:41 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763dea360b041f016dd44796e53426ac4abd09935a5bd152717447cb87ce95ed`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 292.3 KB (292265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c572bd2ea8fca4f65a9229580cea0a899bb90a55db87f84c61a8ebffef6667`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 13.7 MB (13724214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad135b2c91a4bf2f702697c7fbd5036dcc08f117b18dcc1c93853db1c9156a1`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7355f6de608492dfd3b132612c600d5fa83dc5ce8af87565e2b6d4de87bee8ae`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:88d052951d3ddf37819b48fbcbbea4a63a55068a6f0b579856cdf52a8467b6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846adbca1c78516a639189043410b54a25e69a816600c2eaf24d165432872bdc`

```dockerfile
```

-	Layers:
	-	`sha256:6308fac753903c1758b7493a245819edd87f8961363dfe1a9dd151f0c3dc0ba5`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 14.2 KB (14162 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm variant v7

```console
$ docker pull registry@sha256:8576a17b7eee23a767321a9e79151c381398f63d7e9e9cf69ee33bd86b83f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17097032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af2e8909908552324f74e93bbca14ecd788b264c8156d4956d63747c48062bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:17 GMT
ADD alpine-minirootfs-3.21.6-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:17 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:62ed07d04ac65a4abb70fdec446dfb09b05936e34cf361d555b0a75096077e6f`  
		Last Modified: Wed, 28 Jan 2026 01:18:22 GMT  
		Size: 3.1 MB (3099400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa18ffa376327f48a14f6ae18d2b80fa330c68588af0cf68a91e42596027a0`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 291.2 KB (291153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e2cbf4359c687f0d3571dbd8c4abb958cbf1761dd6809cde0aedc90d5e3c4`  
		Last Modified: Wed, 28 Jan 2026 02:55:16 GMT  
		Size: 13.7 MB (13705869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e657a3d99825e81e94450d2630124a0b02d3def4e15dc91abf481d103529c8`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a32d428cb46429981a780aff665401e0b671dcea217cc0238afa6927fd93edb`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:7454d4e7fe34c3c04e2657fc1dc991bbab866c68eac8a86452db36f18fc08ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 KB (280449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da41a8997558bc221dff9d17c571d047258e43df1d49f782b1605a671214cb`

```dockerfile
```

-	Layers:
	-	`sha256:6791213704956ff6075e8b35cc1bc58295c8ed3e0964d7daf017367dd4b0504e`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 266.1 KB (266071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f7fb3a1db5d1b8e584dc40cea74d4e42d9f8c4497ce8800cc1551331e00acd`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 14.4 KB (14378 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:832ef18332f0dde1edff9b45d796231c68f9b9108cf91acb5e6fac450b8fbdcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17777061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5ec5015badd603680de78accbba6eb3e9146f4d642a7ccef64205e55ac518f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:37:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:37:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a52a06d47e0bd39faa08762021bcd609a477f5e8f78d4fa8c57ffe18287a848`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 294.0 KB (294046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc3d49277b720f6fdbd106877ec83cf628b39046dbc4f247520819de0f7a85e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 13.5 MB (13489523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5971fe294ac79298e35f7f9d97ce5bc75257a4c3eb702c6dffae91750bc31`  
		Last Modified: Wed, 28 Jan 2026 02:37:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7580d074a58b8b5b52a2e6921e9c026f1648c513408343beda0685efd062e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:adbebf3dafa2d908f09e4a5754e0f7ad833f5c2496be9ade72fc21b2b722a8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b46989c4e39283845e4c2dce30e6a63a3ba29a1e7479fcca32672e77334469e`

```dockerfile
```

-	Layers:
	-	`sha256:dd86cf8970f88b0aa0c05f3e30fc7fa32919c0d788e81755f6c0c7df3ebdc4f7`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 266.9 KB (266855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5203da2207ac0404783b5d62aaa75a0ab9aa09108ab71c287abeb09e455d0b`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; ppc64le

```console
$ docker pull registry@sha256:618315ffba4956ed8d5d70de0551b2dcfb6e2a452135ae99f1c07ee7447f9a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17039023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a193194a211ebfde6d10572836185b317a5f43ecbf136ef1689bfa9173501c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:37 GMT
ADD alpine-minirootfs-3.21.6-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:37 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:58:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:58:56 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:58:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:56 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:8042a34ff038331b4b3989ada093520db3bf1a93fddb408f83f2f2eae2c4a5c0`  
		Last Modified: Wed, 28 Jan 2026 01:17:48 GMT  
		Size: 3.6 MB (3575435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78725dfca013303f77b35532f05edbf6f602ea442a78c3910ed46da7d0d1941`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 294.5 KB (294500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6fc60e328aa832ca51aa4d28e519274a22e96e965c6adaf65609fbfa982be`  
		Last Modified: Wed, 28 Jan 2026 03:59:11 GMT  
		Size: 13.2 MB (13168478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd21de074d2a9efdc3e8725570ec3a606b586894fde345f033d8015f3824d279`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592530977bbf070854621f0da17736eafcd746657ba8c6000f7ca0d9e458c9c4`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:730aa28d9f8636f8c58a37549dcadfe0f00c5ae3c2877e9ed25a14205e5525cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874e829867de002bd3cd4354aa0cab6d9f4ac5b8fcc23dd21686d51095737a3a`

```dockerfile
```

-	Layers:
	-	`sha256:71148af770f0c346fec319b8310341516f9194c0256a42f76604cf02887e7768`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 264.9 KB (264882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8526c79e63e9c46238d1ac2515ee2085041ba3e878cacaadec7ea816ab03fc8d`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; riscv64

```console
$ docker pull registry@sha256:3cf222ca0fb6fa2f48be588c9bc4fca357ec11e40e9aef984006be37dd012c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199c8d378c70887c6a78b045f8df591b16e1f6719a00d6b4c39c5ec029d45fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 03:52:05 GMT
ADD alpine-minirootfs-3.21.6-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:52:05 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:55:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
VOLUME [/var/lib/registry]
# Thu, 29 Jan 2026 18:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 29 Jan 2026 18:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d9004d3bcc0dc8e7661e1984e1d95b59d7ae869e3d04a461926d42455ebac19f`  
		Last Modified: Wed, 28 Jan 2026 03:52:37 GMT  
		Size: 3.4 MB (3351733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb9a7e4075fd2fc1ab7809801fd801a08706b64f390697ea725f2ce2b350410`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 291.4 KB (291447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2617b27f0af81112ca14a2449d6c62ed6a2cba69183fe1ac7bc9fe967ed59`  
		Last Modified: Thu, 29 Jan 2026 18:56:06 GMT  
		Size: 13.9 MB (13890096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac22fd769e7d2092622684b87d0d18c12fd54307c4b049a76265034d636cf98`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feceefdce15097e8a4c997b866472e8ef9449973b7592562af95c1c9b32f3a3e`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:d6f2d62ca1f8fb89dcb1e3d6a7707cee9ffa9508b0481637b842d362a130c8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2eca841dfa4d4df7863ac8ee8e2517b0d2cf249340b4d1005c4babd0788af3`

```dockerfile
```

-	Layers:
	-	`sha256:a881ba63ddece3f7b83b027933411a41925b68ddecc0861ce31a00fec5f3c6da`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 264.9 KB (264878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4594f425fab54f06397027e5807b656e62c8f5067a45c9578d1256b9899c1302`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; s390x

```console
$ docker pull registry@sha256:c33498ba89378c99374452a7845a7f647360afe831e162027f2a45a8b37c8ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17824058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b08f480eb740d6c1ca794c57b95d3d2751405997ef7fdb5c71158af33da6866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:04 GMT
ADD alpine-minirootfs-3.21.6-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:05:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:05:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:52add0d7fb253eab9140ecb5c50cce4fc1e199637a1ecba6f7e74d9e3cc0f5a2`  
		Last Modified: Wed, 28 Jan 2026 01:17:14 GMT  
		Size: 3.5 MB (3467409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee235944fb00518627ebd0717f92da50bb772669767c7816cce012e4cdfb49e`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 292.1 KB (292092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a4f57dff2ad1e86d79e0b3851d39581aeb57e3a86b5cdcde153d435903254`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.1 MB (14063947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed47b99e41c6b27d2181bd1e86d2ba2ef4d2f38ac9de3f460d6fad3cf960283f`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429e4470dce4dabbdfec93bd8c032800ffc320ee470761bec9a3ed33f61c1187`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:6366730eb32371498787b1d3fbcf5fbbbe59224ee3664101c0b62f4337545b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 KB (279133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b08a5b4bfc851cd4465fe15c4276b5eb1bd07813a27838aab41298ef106b9`

```dockerfile
```

-	Layers:
	-	`sha256:fc787f230350822bf70286bc7dcc86b05a9131c975bf175ae8ddbcfc114df0ac`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 264.8 KB (264848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c8a51b4229dcc44d1cec9b84b70d854f11a9004474c7caeb9ee6ff71dfe043`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0`

```console
$ docker pull registry@sha256:6c5666b861f3505b116bb9aa9b25175e71210414bd010d92035ff64018f9457e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.0` - linux; amd64

```console
$ docker pull registry@sha256:5b12b22f21522fe69443079df04c0f3f42cb9977857f3c20404386652a6c6d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18549482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b916d8206bcbfc54c95fb06076751932c902254277f149b082dd5d4d67fccb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:36:15 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:36:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:15 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2f893a11eee550abbadc144efb3cccc151908f28f8a20775e6e990065d8b34`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 291.1 KB (291125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeded8eec5f8394cf132cd851680a68d0861eacaeb3dfdce2df957303cb5beb`  
		Last Modified: Wed, 28 Jan 2026 02:36:23 GMT  
		Size: 14.6 MB (14614005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8100d968019ced9a7dccd30207ff9e8781702aadbc3f409202021fb98aad4ef`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369e5bd3505f549f6bbad4856b935f10097b8cfb09774ca9064e510a9435ba0`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:c80f16a2e278a83f48c54afb114e4838086b2c88dce0924c0fbc4346cd9a694d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 KB (281083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2137385e84d71cfe37712458553b58efc2b14294c63c72c30fac3ee8936e00f8`

```dockerfile
```

-	Layers:
	-	`sha256:e7513cd118306c3b5d92385ed98fc5c801062e5d43ec34751fdcce10f5287e1e`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 266.8 KB (266799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db921fed581e221e8c8e3a194d71ead75542a129e98d77afa02dc58759fba749`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; arm variant v6

```console
$ docker pull registry@sha256:c2540c3e0f60b6f222233fe4f1c8c4f70ec75168bb2bcbaf901ec5c3408ff50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17382960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3acf3750b01ad98f470e0f16647a8765fe4abd2149b70dab4cbd11dc07f0ac7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:56:41 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:56:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:41 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763dea360b041f016dd44796e53426ac4abd09935a5bd152717447cb87ce95ed`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 292.3 KB (292265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c572bd2ea8fca4f65a9229580cea0a899bb90a55db87f84c61a8ebffef6667`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 13.7 MB (13724214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad135b2c91a4bf2f702697c7fbd5036dcc08f117b18dcc1c93853db1c9156a1`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7355f6de608492dfd3b132612c600d5fa83dc5ce8af87565e2b6d4de87bee8ae`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:88d052951d3ddf37819b48fbcbbea4a63a55068a6f0b579856cdf52a8467b6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846adbca1c78516a639189043410b54a25e69a816600c2eaf24d165432872bdc`

```dockerfile
```

-	Layers:
	-	`sha256:6308fac753903c1758b7493a245819edd87f8961363dfe1a9dd151f0c3dc0ba5`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 14.2 KB (14162 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; arm variant v7

```console
$ docker pull registry@sha256:8576a17b7eee23a767321a9e79151c381398f63d7e9e9cf69ee33bd86b83f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17097032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af2e8909908552324f74e93bbca14ecd788b264c8156d4956d63747c48062bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:17 GMT
ADD alpine-minirootfs-3.21.6-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:17 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:62ed07d04ac65a4abb70fdec446dfb09b05936e34cf361d555b0a75096077e6f`  
		Last Modified: Wed, 28 Jan 2026 01:18:22 GMT  
		Size: 3.1 MB (3099400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa18ffa376327f48a14f6ae18d2b80fa330c68588af0cf68a91e42596027a0`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 291.2 KB (291153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e2cbf4359c687f0d3571dbd8c4abb958cbf1761dd6809cde0aedc90d5e3c4`  
		Last Modified: Wed, 28 Jan 2026 02:55:16 GMT  
		Size: 13.7 MB (13705869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e657a3d99825e81e94450d2630124a0b02d3def4e15dc91abf481d103529c8`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a32d428cb46429981a780aff665401e0b671dcea217cc0238afa6927fd93edb`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:7454d4e7fe34c3c04e2657fc1dc991bbab866c68eac8a86452db36f18fc08ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 KB (280449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da41a8997558bc221dff9d17c571d047258e43df1d49f782b1605a671214cb`

```dockerfile
```

-	Layers:
	-	`sha256:6791213704956ff6075e8b35cc1bc58295c8ed3e0964d7daf017367dd4b0504e`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 266.1 KB (266071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f7fb3a1db5d1b8e584dc40cea74d4e42d9f8c4497ce8800cc1551331e00acd`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 14.4 KB (14378 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:832ef18332f0dde1edff9b45d796231c68f9b9108cf91acb5e6fac450b8fbdcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17777061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5ec5015badd603680de78accbba6eb3e9146f4d642a7ccef64205e55ac518f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:37:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:37:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a52a06d47e0bd39faa08762021bcd609a477f5e8f78d4fa8c57ffe18287a848`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 294.0 KB (294046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc3d49277b720f6fdbd106877ec83cf628b39046dbc4f247520819de0f7a85e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 13.5 MB (13489523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5971fe294ac79298e35f7f9d97ce5bc75257a4c3eb702c6dffae91750bc31`  
		Last Modified: Wed, 28 Jan 2026 02:37:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7580d074a58b8b5b52a2e6921e9c026f1648c513408343beda0685efd062e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:adbebf3dafa2d908f09e4a5754e0f7ad833f5c2496be9ade72fc21b2b722a8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b46989c4e39283845e4c2dce30e6a63a3ba29a1e7479fcca32672e77334469e`

```dockerfile
```

-	Layers:
	-	`sha256:dd86cf8970f88b0aa0c05f3e30fc7fa32919c0d788e81755f6c0c7df3ebdc4f7`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 266.9 KB (266855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5203da2207ac0404783b5d62aaa75a0ab9aa09108ab71c287abeb09e455d0b`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; ppc64le

```console
$ docker pull registry@sha256:618315ffba4956ed8d5d70de0551b2dcfb6e2a452135ae99f1c07ee7447f9a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17039023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a193194a211ebfde6d10572836185b317a5f43ecbf136ef1689bfa9173501c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:37 GMT
ADD alpine-minirootfs-3.21.6-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:37 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:58:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:58:56 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:58:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:56 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:8042a34ff038331b4b3989ada093520db3bf1a93fddb408f83f2f2eae2c4a5c0`  
		Last Modified: Wed, 28 Jan 2026 01:17:48 GMT  
		Size: 3.6 MB (3575435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78725dfca013303f77b35532f05edbf6f602ea442a78c3910ed46da7d0d1941`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 294.5 KB (294500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6fc60e328aa832ca51aa4d28e519274a22e96e965c6adaf65609fbfa982be`  
		Last Modified: Wed, 28 Jan 2026 03:59:11 GMT  
		Size: 13.2 MB (13168478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd21de074d2a9efdc3e8725570ec3a606b586894fde345f033d8015f3824d279`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592530977bbf070854621f0da17736eafcd746657ba8c6000f7ca0d9e458c9c4`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:730aa28d9f8636f8c58a37549dcadfe0f00c5ae3c2877e9ed25a14205e5525cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874e829867de002bd3cd4354aa0cab6d9f4ac5b8fcc23dd21686d51095737a3a`

```dockerfile
```

-	Layers:
	-	`sha256:71148af770f0c346fec319b8310341516f9194c0256a42f76604cf02887e7768`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 264.9 KB (264882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8526c79e63e9c46238d1ac2515ee2085041ba3e878cacaadec7ea816ab03fc8d`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; riscv64

```console
$ docker pull registry@sha256:3cf222ca0fb6fa2f48be588c9bc4fca357ec11e40e9aef984006be37dd012c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199c8d378c70887c6a78b045f8df591b16e1f6719a00d6b4c39c5ec029d45fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 03:52:05 GMT
ADD alpine-minirootfs-3.21.6-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:52:05 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:55:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
VOLUME [/var/lib/registry]
# Thu, 29 Jan 2026 18:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 29 Jan 2026 18:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d9004d3bcc0dc8e7661e1984e1d95b59d7ae869e3d04a461926d42455ebac19f`  
		Last Modified: Wed, 28 Jan 2026 03:52:37 GMT  
		Size: 3.4 MB (3351733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb9a7e4075fd2fc1ab7809801fd801a08706b64f390697ea725f2ce2b350410`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 291.4 KB (291447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2617b27f0af81112ca14a2449d6c62ed6a2cba69183fe1ac7bc9fe967ed59`  
		Last Modified: Thu, 29 Jan 2026 18:56:06 GMT  
		Size: 13.9 MB (13890096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac22fd769e7d2092622684b87d0d18c12fd54307c4b049a76265034d636cf98`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feceefdce15097e8a4c997b866472e8ef9449973b7592562af95c1c9b32f3a3e`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:d6f2d62ca1f8fb89dcb1e3d6a7707cee9ffa9508b0481637b842d362a130c8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2eca841dfa4d4df7863ac8ee8e2517b0d2cf249340b4d1005c4babd0788af3`

```dockerfile
```

-	Layers:
	-	`sha256:a881ba63ddece3f7b83b027933411a41925b68ddecc0861ce31a00fec5f3c6da`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 264.9 KB (264878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4594f425fab54f06397027e5807b656e62c8f5067a45c9578d1256b9899c1302`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; s390x

```console
$ docker pull registry@sha256:c33498ba89378c99374452a7845a7f647360afe831e162027f2a45a8b37c8ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17824058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b08f480eb740d6c1ca794c57b95d3d2751405997ef7fdb5c71158af33da6866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:04 GMT
ADD alpine-minirootfs-3.21.6-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:05:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:05:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:52add0d7fb253eab9140ecb5c50cce4fc1e199637a1ecba6f7e74d9e3cc0f5a2`  
		Last Modified: Wed, 28 Jan 2026 01:17:14 GMT  
		Size: 3.5 MB (3467409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee235944fb00518627ebd0717f92da50bb772669767c7816cce012e4cdfb49e`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 292.1 KB (292092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a4f57dff2ad1e86d79e0b3851d39581aeb57e3a86b5cdcde153d435903254`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.1 MB (14063947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed47b99e41c6b27d2181bd1e86d2ba2ef4d2f38ac9de3f460d6fad3cf960283f`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429e4470dce4dabbdfec93bd8c032800ffc320ee470761bec9a3ed33f61c1187`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:6366730eb32371498787b1d3fbcf5fbbbe59224ee3664101c0b62f4337545b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 KB (279133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b08a5b4bfc851cd4465fe15c4276b5eb1bd07813a27838aab41298ef106b9`

```dockerfile
```

-	Layers:
	-	`sha256:fc787f230350822bf70286bc7dcc86b05a9131c975bf175ae8ddbcfc114df0ac`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 264.8 KB (264848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c8a51b4229dcc44d1cec9b84b70d854f11a9004474c7caeb9ee6ff71dfe043`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0`

```console
$ docker pull registry@sha256:6c5666b861f3505b116bb9aa9b25175e71210414bd010d92035ff64018f9457e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.0.0` - linux; amd64

```console
$ docker pull registry@sha256:5b12b22f21522fe69443079df04c0f3f42cb9977857f3c20404386652a6c6d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18549482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b916d8206bcbfc54c95fb06076751932c902254277f149b082dd5d4d67fccb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:36:15 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:36:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:15 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2f893a11eee550abbadc144efb3cccc151908f28f8a20775e6e990065d8b34`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 291.1 KB (291125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeded8eec5f8394cf132cd851680a68d0861eacaeb3dfdce2df957303cb5beb`  
		Last Modified: Wed, 28 Jan 2026 02:36:23 GMT  
		Size: 14.6 MB (14614005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8100d968019ced9a7dccd30207ff9e8781702aadbc3f409202021fb98aad4ef`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369e5bd3505f549f6bbad4856b935f10097b8cfb09774ca9064e510a9435ba0`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:c80f16a2e278a83f48c54afb114e4838086b2c88dce0924c0fbc4346cd9a694d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 KB (281083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2137385e84d71cfe37712458553b58efc2b14294c63c72c30fac3ee8936e00f8`

```dockerfile
```

-	Layers:
	-	`sha256:e7513cd118306c3b5d92385ed98fc5c801062e5d43ec34751fdcce10f5287e1e`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 266.8 KB (266799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db921fed581e221e8c8e3a194d71ead75542a129e98d77afa02dc58759fba749`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; arm variant v6

```console
$ docker pull registry@sha256:c2540c3e0f60b6f222233fe4f1c8c4f70ec75168bb2bcbaf901ec5c3408ff50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17382960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3acf3750b01ad98f470e0f16647a8765fe4abd2149b70dab4cbd11dc07f0ac7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:56:41 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:56:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:41 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763dea360b041f016dd44796e53426ac4abd09935a5bd152717447cb87ce95ed`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 292.3 KB (292265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c572bd2ea8fca4f65a9229580cea0a899bb90a55db87f84c61a8ebffef6667`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 13.7 MB (13724214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad135b2c91a4bf2f702697c7fbd5036dcc08f117b18dcc1c93853db1c9156a1`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7355f6de608492dfd3b132612c600d5fa83dc5ce8af87565e2b6d4de87bee8ae`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:88d052951d3ddf37819b48fbcbbea4a63a55068a6f0b579856cdf52a8467b6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846adbca1c78516a639189043410b54a25e69a816600c2eaf24d165432872bdc`

```dockerfile
```

-	Layers:
	-	`sha256:6308fac753903c1758b7493a245819edd87f8961363dfe1a9dd151f0c3dc0ba5`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 14.2 KB (14162 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; arm variant v7

```console
$ docker pull registry@sha256:8576a17b7eee23a767321a9e79151c381398f63d7e9e9cf69ee33bd86b83f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17097032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af2e8909908552324f74e93bbca14ecd788b264c8156d4956d63747c48062bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:17 GMT
ADD alpine-minirootfs-3.21.6-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:17 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:62ed07d04ac65a4abb70fdec446dfb09b05936e34cf361d555b0a75096077e6f`  
		Last Modified: Wed, 28 Jan 2026 01:18:22 GMT  
		Size: 3.1 MB (3099400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa18ffa376327f48a14f6ae18d2b80fa330c68588af0cf68a91e42596027a0`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 291.2 KB (291153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e2cbf4359c687f0d3571dbd8c4abb958cbf1761dd6809cde0aedc90d5e3c4`  
		Last Modified: Wed, 28 Jan 2026 02:55:16 GMT  
		Size: 13.7 MB (13705869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e657a3d99825e81e94450d2630124a0b02d3def4e15dc91abf481d103529c8`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a32d428cb46429981a780aff665401e0b671dcea217cc0238afa6927fd93edb`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:7454d4e7fe34c3c04e2657fc1dc991bbab866c68eac8a86452db36f18fc08ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 KB (280449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da41a8997558bc221dff9d17c571d047258e43df1d49f782b1605a671214cb`

```dockerfile
```

-	Layers:
	-	`sha256:6791213704956ff6075e8b35cc1bc58295c8ed3e0964d7daf017367dd4b0504e`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 266.1 KB (266071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f7fb3a1db5d1b8e584dc40cea74d4e42d9f8c4497ce8800cc1551331e00acd`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 14.4 KB (14378 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:832ef18332f0dde1edff9b45d796231c68f9b9108cf91acb5e6fac450b8fbdcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17777061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5ec5015badd603680de78accbba6eb3e9146f4d642a7ccef64205e55ac518f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:37:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:37:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a52a06d47e0bd39faa08762021bcd609a477f5e8f78d4fa8c57ffe18287a848`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 294.0 KB (294046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc3d49277b720f6fdbd106877ec83cf628b39046dbc4f247520819de0f7a85e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 13.5 MB (13489523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5971fe294ac79298e35f7f9d97ce5bc75257a4c3eb702c6dffae91750bc31`  
		Last Modified: Wed, 28 Jan 2026 02:37:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7580d074a58b8b5b52a2e6921e9c026f1648c513408343beda0685efd062e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:adbebf3dafa2d908f09e4a5754e0f7ad833f5c2496be9ade72fc21b2b722a8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b46989c4e39283845e4c2dce30e6a63a3ba29a1e7479fcca32672e77334469e`

```dockerfile
```

-	Layers:
	-	`sha256:dd86cf8970f88b0aa0c05f3e30fc7fa32919c0d788e81755f6c0c7df3ebdc4f7`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 266.9 KB (266855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5203da2207ac0404783b5d62aaa75a0ab9aa09108ab71c287abeb09e455d0b`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; ppc64le

```console
$ docker pull registry@sha256:618315ffba4956ed8d5d70de0551b2dcfb6e2a452135ae99f1c07ee7447f9a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17039023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a193194a211ebfde6d10572836185b317a5f43ecbf136ef1689bfa9173501c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:37 GMT
ADD alpine-minirootfs-3.21.6-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:37 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:58:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:58:56 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:58:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:56 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:8042a34ff038331b4b3989ada093520db3bf1a93fddb408f83f2f2eae2c4a5c0`  
		Last Modified: Wed, 28 Jan 2026 01:17:48 GMT  
		Size: 3.6 MB (3575435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78725dfca013303f77b35532f05edbf6f602ea442a78c3910ed46da7d0d1941`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 294.5 KB (294500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6fc60e328aa832ca51aa4d28e519274a22e96e965c6adaf65609fbfa982be`  
		Last Modified: Wed, 28 Jan 2026 03:59:11 GMT  
		Size: 13.2 MB (13168478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd21de074d2a9efdc3e8725570ec3a606b586894fde345f033d8015f3824d279`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592530977bbf070854621f0da17736eafcd746657ba8c6000f7ca0d9e458c9c4`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:730aa28d9f8636f8c58a37549dcadfe0f00c5ae3c2877e9ed25a14205e5525cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874e829867de002bd3cd4354aa0cab6d9f4ac5b8fcc23dd21686d51095737a3a`

```dockerfile
```

-	Layers:
	-	`sha256:71148af770f0c346fec319b8310341516f9194c0256a42f76604cf02887e7768`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 264.9 KB (264882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8526c79e63e9c46238d1ac2515ee2085041ba3e878cacaadec7ea816ab03fc8d`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; riscv64

```console
$ docker pull registry@sha256:3cf222ca0fb6fa2f48be588c9bc4fca357ec11e40e9aef984006be37dd012c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199c8d378c70887c6a78b045f8df591b16e1f6719a00d6b4c39c5ec029d45fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 03:52:05 GMT
ADD alpine-minirootfs-3.21.6-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:52:05 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:55:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
VOLUME [/var/lib/registry]
# Thu, 29 Jan 2026 18:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 29 Jan 2026 18:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d9004d3bcc0dc8e7661e1984e1d95b59d7ae869e3d04a461926d42455ebac19f`  
		Last Modified: Wed, 28 Jan 2026 03:52:37 GMT  
		Size: 3.4 MB (3351733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb9a7e4075fd2fc1ab7809801fd801a08706b64f390697ea725f2ce2b350410`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 291.4 KB (291447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2617b27f0af81112ca14a2449d6c62ed6a2cba69183fe1ac7bc9fe967ed59`  
		Last Modified: Thu, 29 Jan 2026 18:56:06 GMT  
		Size: 13.9 MB (13890096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac22fd769e7d2092622684b87d0d18c12fd54307c4b049a76265034d636cf98`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feceefdce15097e8a4c997b866472e8ef9449973b7592562af95c1c9b32f3a3e`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:d6f2d62ca1f8fb89dcb1e3d6a7707cee9ffa9508b0481637b842d362a130c8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2eca841dfa4d4df7863ac8ee8e2517b0d2cf249340b4d1005c4babd0788af3`

```dockerfile
```

-	Layers:
	-	`sha256:a881ba63ddece3f7b83b027933411a41925b68ddecc0861ce31a00fec5f3c6da`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 264.9 KB (264878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4594f425fab54f06397027e5807b656e62c8f5067a45c9578d1256b9899c1302`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; s390x

```console
$ docker pull registry@sha256:c33498ba89378c99374452a7845a7f647360afe831e162027f2a45a8b37c8ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17824058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b08f480eb740d6c1ca794c57b95d3d2751405997ef7fdb5c71158af33da6866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:04 GMT
ADD alpine-minirootfs-3.21.6-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:05:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:05:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:52add0d7fb253eab9140ecb5c50cce4fc1e199637a1ecba6f7e74d9e3cc0f5a2`  
		Last Modified: Wed, 28 Jan 2026 01:17:14 GMT  
		Size: 3.5 MB (3467409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee235944fb00518627ebd0717f92da50bb772669767c7816cce012e4cdfb49e`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 292.1 KB (292092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a4f57dff2ad1e86d79e0b3851d39581aeb57e3a86b5cdcde153d435903254`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.1 MB (14063947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed47b99e41c6b27d2181bd1e86d2ba2ef4d2f38ac9de3f460d6fad3cf960283f`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429e4470dce4dabbdfec93bd8c032800ffc320ee470761bec9a3ed33f61c1187`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:6366730eb32371498787b1d3fbcf5fbbbe59224ee3664101c0b62f4337545b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 KB (279133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b08a5b4bfc851cd4465fe15c4276b5eb1bd07813a27838aab41298ef106b9`

```dockerfile
```

-	Layers:
	-	`sha256:fc787f230350822bf70286bc7dcc86b05a9131c975bf175ae8ddbcfc114df0ac`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 264.8 KB (264848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c8a51b4229dcc44d1cec9b84b70d854f11a9004474c7caeb9ee6ff71dfe043`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:6c5666b861f3505b116bb9aa9b25175e71210414bd010d92035ff64018f9457e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:5b12b22f21522fe69443079df04c0f3f42cb9977857f3c20404386652a6c6d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18549482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b916d8206bcbfc54c95fb06076751932c902254277f149b082dd5d4d67fccb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:36:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:36:15 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:36:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:36:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:36:15 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2f893a11eee550abbadc144efb3cccc151908f28f8a20775e6e990065d8b34`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 291.1 KB (291125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeded8eec5f8394cf132cd851680a68d0861eacaeb3dfdce2df957303cb5beb`  
		Last Modified: Wed, 28 Jan 2026 02:36:23 GMT  
		Size: 14.6 MB (14614005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8100d968019ced9a7dccd30207ff9e8781702aadbc3f409202021fb98aad4ef`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369e5bd3505f549f6bbad4856b935f10097b8cfb09774ca9064e510a9435ba0`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:c80f16a2e278a83f48c54afb114e4838086b2c88dce0924c0fbc4346cd9a694d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 KB (281083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2137385e84d71cfe37712458553b58efc2b14294c63c72c30fac3ee8936e00f8`

```dockerfile
```

-	Layers:
	-	`sha256:e7513cd118306c3b5d92385ed98fc5c801062e5d43ec34751fdcce10f5287e1e`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 266.8 KB (266799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db921fed581e221e8c8e3a194d71ead75542a129e98d77afa02dc58759fba749`  
		Last Modified: Wed, 28 Jan 2026 02:36:22 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:c2540c3e0f60b6f222233fe4f1c8c4f70ec75168bb2bcbaf901ec5c3408ff50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17382960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3acf3750b01ad98f470e0f16647a8765fe4abd2149b70dab4cbd11dc07f0ac7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:56:41 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:56:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:41 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763dea360b041f016dd44796e53426ac4abd09935a5bd152717447cb87ce95ed`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 292.3 KB (292265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c572bd2ea8fca4f65a9229580cea0a899bb90a55db87f84c61a8ebffef6667`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 13.7 MB (13724214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad135b2c91a4bf2f702697c7fbd5036dcc08f117b18dcc1c93853db1c9156a1`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7355f6de608492dfd3b132612c600d5fa83dc5ce8af87565e2b6d4de87bee8ae`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:88d052951d3ddf37819b48fbcbbea4a63a55068a6f0b579856cdf52a8467b6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846adbca1c78516a639189043410b54a25e69a816600c2eaf24d165432872bdc`

```dockerfile
```

-	Layers:
	-	`sha256:6308fac753903c1758b7493a245819edd87f8961363dfe1a9dd151f0c3dc0ba5`  
		Last Modified: Wed, 28 Jan 2026 02:56:46 GMT  
		Size: 14.2 KB (14162 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:8576a17b7eee23a767321a9e79151c381398f63d7e9e9cf69ee33bd86b83f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17097032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af2e8909908552324f74e93bbca14ecd788b264c8156d4956d63747c48062bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:17 GMT
ADD alpine-minirootfs-3.21.6-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:17 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:62ed07d04ac65a4abb70fdec446dfb09b05936e34cf361d555b0a75096077e6f`  
		Last Modified: Wed, 28 Jan 2026 01:18:22 GMT  
		Size: 3.1 MB (3099400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa18ffa376327f48a14f6ae18d2b80fa330c68588af0cf68a91e42596027a0`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 291.2 KB (291153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e2cbf4359c687f0d3571dbd8c4abb958cbf1761dd6809cde0aedc90d5e3c4`  
		Last Modified: Wed, 28 Jan 2026 02:55:16 GMT  
		Size: 13.7 MB (13705869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e657a3d99825e81e94450d2630124a0b02d3def4e15dc91abf481d103529c8`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a32d428cb46429981a780aff665401e0b671dcea217cc0238afa6927fd93edb`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:7454d4e7fe34c3c04e2657fc1dc991bbab866c68eac8a86452db36f18fc08ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 KB (280449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da41a8997558bc221dff9d17c571d047258e43df1d49f782b1605a671214cb`

```dockerfile
```

-	Layers:
	-	`sha256:6791213704956ff6075e8b35cc1bc58295c8ed3e0964d7daf017367dd4b0504e`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 266.1 KB (266071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f7fb3a1db5d1b8e584dc40cea74d4e42d9f8c4497ce8800cc1551331e00acd`  
		Last Modified: Wed, 28 Jan 2026 02:55:15 GMT  
		Size: 14.4 KB (14378 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:832ef18332f0dde1edff9b45d796231c68f9b9108cf91acb5e6fac450b8fbdcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17777061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5ec5015badd603680de78accbba6eb3e9146f4d642a7ccef64205e55ac518f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:37:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 02:37:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 02:37:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:37:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:37:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a52a06d47e0bd39faa08762021bcd609a477f5e8f78d4fa8c57ffe18287a848`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 294.0 KB (294046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc3d49277b720f6fdbd106877ec83cf628b39046dbc4f247520819de0f7a85e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 13.5 MB (13489523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5971fe294ac79298e35f7f9d97ce5bc75257a4c3eb702c6dffae91750bc31`  
		Last Modified: Wed, 28 Jan 2026 02:37:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7580d074a58b8b5b52a2e6921e9c026f1648c513408343beda0685efd062e`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:adbebf3dafa2d908f09e4a5754e0f7ad833f5c2496be9ade72fc21b2b722a8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 KB (281259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b46989c4e39283845e4c2dce30e6a63a3ba29a1e7479fcca32672e77334469e`

```dockerfile
```

-	Layers:
	-	`sha256:dd86cf8970f88b0aa0c05f3e30fc7fa32919c0d788e81755f6c0c7df3ebdc4f7`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 266.9 KB (266855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5203da2207ac0404783b5d62aaa75a0ab9aa09108ab71c287abeb09e455d0b`  
		Last Modified: Wed, 28 Jan 2026 02:37:27 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:618315ffba4956ed8d5d70de0551b2dcfb6e2a452135ae99f1c07ee7447f9a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17039023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a193194a211ebfde6d10572836185b317a5f43ecbf136ef1689bfa9173501c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:37 GMT
ADD alpine-minirootfs-3.21.6-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:37 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:58:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:58:56 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:58:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:58:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:56 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:8042a34ff038331b4b3989ada093520db3bf1a93fddb408f83f2f2eae2c4a5c0`  
		Last Modified: Wed, 28 Jan 2026 01:17:48 GMT  
		Size: 3.6 MB (3575435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78725dfca013303f77b35532f05edbf6f602ea442a78c3910ed46da7d0d1941`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 294.5 KB (294500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6fc60e328aa832ca51aa4d28e519274a22e96e965c6adaf65609fbfa982be`  
		Last Modified: Wed, 28 Jan 2026 03:59:11 GMT  
		Size: 13.2 MB (13168478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd21de074d2a9efdc3e8725570ec3a606b586894fde345f033d8015f3824d279`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592530977bbf070854621f0da17736eafcd746657ba8c6000f7ca0d9e458c9c4`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:730aa28d9f8636f8c58a37549dcadfe0f00c5ae3c2877e9ed25a14205e5525cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874e829867de002bd3cd4354aa0cab6d9f4ac5b8fcc23dd21686d51095737a3a`

```dockerfile
```

-	Layers:
	-	`sha256:71148af770f0c346fec319b8310341516f9194c0256a42f76604cf02887e7768`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 264.9 KB (264882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8526c79e63e9c46238d1ac2515ee2085041ba3e878cacaadec7ea816ab03fc8d`  
		Last Modified: Wed, 28 Jan 2026 03:59:10 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; riscv64

```console
$ docker pull registry@sha256:3cf222ca0fb6fa2f48be588c9bc4fca357ec11e40e9aef984006be37dd012c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199c8d378c70887c6a78b045f8df591b16e1f6719a00d6b4c39c5ec029d45fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 03:52:05 GMT
ADD alpine-minirootfs-3.21.6-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:52:05 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 18:55:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
VOLUME [/var/lib/registry]
# Thu, 29 Jan 2026 18:55:08 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 29 Jan 2026 18:55:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 18:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jan 2026 18:55:08 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d9004d3bcc0dc8e7661e1984e1d95b59d7ae869e3d04a461926d42455ebac19f`  
		Last Modified: Wed, 28 Jan 2026 03:52:37 GMT  
		Size: 3.4 MB (3351733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb9a7e4075fd2fc1ab7809801fd801a08706b64f390697ea725f2ce2b350410`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 291.4 KB (291447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2617b27f0af81112ca14a2449d6c62ed6a2cba69183fe1ac7bc9fe967ed59`  
		Last Modified: Thu, 29 Jan 2026 18:56:06 GMT  
		Size: 13.9 MB (13890096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac22fd769e7d2092622684b87d0d18c12fd54307c4b049a76265034d636cf98`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feceefdce15097e8a4c997b866472e8ef9449973b7592562af95c1c9b32f3a3e`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:d6f2d62ca1f8fb89dcb1e3d6a7707cee9ffa9508b0481637b842d362a130c8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 KB (279208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2eca841dfa4d4df7863ac8ee8e2517b0d2cf249340b4d1005c4babd0788af3`

```dockerfile
```

-	Layers:
	-	`sha256:a881ba63ddece3f7b83b027933411a41925b68ddecc0861ce31a00fec5f3c6da`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 264.9 KB (264878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4594f425fab54f06397027e5807b656e62c8f5067a45c9578d1256b9899c1302`  
		Last Modified: Thu, 29 Jan 2026 18:56:04 GMT  
		Size: 14.3 KB (14330 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:c33498ba89378c99374452a7845a7f647360afe831e162027f2a45a8b37c8ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17824058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b08f480eb740d6c1ca794c57b95d3d2751405997ef7fdb5c71158af33da6866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:04 GMT
ADD alpine-minirootfs-3.21.6-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:05:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
VOLUME [/var/lib/registry]
# Wed, 28 Jan 2026 03:05:19 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 28 Jan 2026 03:05:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:05:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:05:19 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:52add0d7fb253eab9140ecb5c50cce4fc1e199637a1ecba6f7e74d9e3cc0f5a2`  
		Last Modified: Wed, 28 Jan 2026 01:17:14 GMT  
		Size: 3.5 MB (3467409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee235944fb00518627ebd0717f92da50bb772669767c7816cce012e4cdfb49e`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 292.1 KB (292092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a4f57dff2ad1e86d79e0b3851d39581aeb57e3a86b5cdcde153d435903254`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.1 MB (14063947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed47b99e41c6b27d2181bd1e86d2ba2ef4d2f38ac9de3f460d6fad3cf960283f`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429e4470dce4dabbdfec93bd8c032800ffc320ee470761bec9a3ed33f61c1187`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:6366730eb32371498787b1d3fbcf5fbbbe59224ee3664101c0b62f4337545b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 KB (279133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b08a5b4bfc851cd4465fe15c4276b5eb1bd07813a27838aab41298ef106b9`

```dockerfile
```

-	Layers:
	-	`sha256:fc787f230350822bf70286bc7dcc86b05a9131c975bf175ae8ddbcfc114df0ac`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 264.8 KB (264848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c8a51b4229dcc44d1cec9b84b70d854f11a9004474c7caeb9ee6ff71dfe043`  
		Last Modified: Wed, 28 Jan 2026 03:05:32 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
