## `rust:alpine`

```console
$ docker pull rust@sha256:69d7b9d9aeaf108a1419d9a7fcf7860dcc043e9dbd1ab7ce88e44228774d99e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:6f37c2b56fde862a67116c4bddbb6014c0a758b24944f8650c8ff8c735f96f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346352466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6336bf7b311135c893a4a930b0920892b5e596ccdc374777290fa91bb59ae818`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:48:01 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 28 Jan 2026 03:48:01 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 28 Jan 2026 03:48:01 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Wed, 28 Jan 2026 03:48:20 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cb3bc09ef100528982994e39af3d1ffc9736d148a946e22f198f47bb2606ed`  
		Last Modified: Wed, 28 Jan 2026 03:48:57 GMT  
		Size: 75.1 MB (75119103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35751de1c97a41793e5081e5588653cca0eb71d8252008b728aac03e453f6654`  
		Last Modified: Wed, 28 Jan 2026 03:49:00 GMT  
		Size: 267.4 MB (267371542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:73ba137446db1e731dcf80027ea405ff697fd8bc6212cff21cd9df0c49a30536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1021805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48559c517148664cace76490970315c34f3f957ddce041049783c2651b8eef0f`

```dockerfile
```

-	Layers:
	-	`sha256:637430eb400cfc6b9e77387fe80819b48ad3fb74fc9486d9951727a7a0f35690`  
		Last Modified: Wed, 28 Jan 2026 03:48:54 GMT  
		Size: 1.0 MB (1008415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9013daa67831a9a390db8bd371f0f4433ee1ceb339fb6692743075066867f6`  
		Last Modified: Wed, 28 Jan 2026 03:48:53 GMT  
		Size: 13.4 KB (13390 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b2769c726e0c34d508368501a3378aab00b7a8522b1b5b7e603f45ea0449b03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344536334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0428561e400208f36725122ec18461b5fe6a58663429968a49cbd6e2c20c6c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:55:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 28 Jan 2026 03:55:26 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 28 Jan 2026 03:55:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Wed, 28 Jan 2026 03:55:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba5aec2e11460185e520d0178ac6a6aadc8b3e392395341b1399b2490ec5c3e`  
		Last Modified: Wed, 28 Jan 2026 03:56:24 GMT  
		Size: 66.5 MB (66542802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412b37f4077a94417a3e0d7534d6c441031c0d2bbd05a5231332c3d7d14deb0e`  
		Last Modified: Wed, 28 Jan 2026 03:56:28 GMT  
		Size: 273.8 MB (273796441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:9a93a4e86a26e67f917a81f72b3c66a030ff384064147cb9e4128f6b9ad80a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1081030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43334f46e451766d547b2341d0c5a502729acf7f0a36ca987b1dfe2427c4f1a4`

```dockerfile
```

-	Layers:
	-	`sha256:ddae6c86ba7db85be064142141271c8a74a7679e6da6c59529ef5588955c9870`  
		Last Modified: Wed, 28 Jan 2026 03:56:21 GMT  
		Size: 1.1 MB (1067474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c48d7565697d62dd7976dba820c0623879cfdc4dd2a50323df1d55019f3ddad`  
		Last Modified: Wed, 28 Jan 2026 03:56:21 GMT  
		Size: 13.6 KB (13556 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:5d297fe333cf2f323763576c4ac012f7e76e5dd2bc78611b454144965698aa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362622651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819fd8e846b68d6c13c2b02762bd0afe8ec5c8986ec24f08b34b25f749d3d3e9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 05:48:47 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 28 Jan 2026 05:48:47 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 28 Jan 2026 05:48:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Wed, 28 Jan 2026 05:49:11 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348db6f6ce4492f935a268feb267f418c6f5f05e5c3f88db31ba8be4d6f3ed7f`  
		Last Modified: Wed, 28 Jan 2026 05:50:23 GMT  
		Size: 66.4 MB (66425966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b76046878370da3b49ce3eb9cccf077c6d7de4c98ff750874320a59833ad6`  
		Last Modified: Wed, 28 Jan 2026 05:50:27 GMT  
		Size: 292.4 MB (292367042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:a4b5677cbd09acd4599d4f0ee2d74267fda75879f2f83a3b8e9f1e83d6b5d0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d9e099cc907ab3a4598dec0c8cd348169c81a0038e9618c71682528c365468`

```dockerfile
```

-	Layers:
	-	`sha256:90091c9f2de364bfc1eef48dfc2376dc20f3791aa0b9c86fd29496968089faa2`  
		Last Modified: Wed, 28 Jan 2026 05:50:20 GMT  
		Size: 1000.8 KB (1000761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31ac7bd8ff8db9ad961de89775f79966a0e511a1586fe864592c9b5edf62f20`  
		Last Modified: Wed, 28 Jan 2026 05:50:19 GMT  
		Size: 13.5 KB (13460 bytes)  
		MIME: application/vnd.in-toto+json
