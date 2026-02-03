## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:66e45ca090b7d2424b1ab4366d308ebff31906a36309bd097dacdc2e531cd9c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:387924d19d691861ffdcf1d50dc63b4b288c65873ef2bf06763e94a51a821f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329780841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212fb5a7b37002e2d0dbcc21333331e0d6a58f9762292776382ff87d077cf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:46:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 28 Jan 2026 03:46:27 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 28 Jan 2026 03:46:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Wed, 28 Jan 2026 03:46:49 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb1c433422ebea1048a86771cc8a7444a28199d422037e563b3937d806a2b4`  
		Last Modified: Wed, 28 Jan 2026 03:47:28 GMT  
		Size: 58.8 MB (58781744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bedd2f0f0138be2794267e7309e81846aa285ecb03de7ccae58c5b1d051754b`  
		Last Modified: Wed, 28 Jan 2026 03:47:32 GMT  
		Size: 267.4 MB (267371233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:4cd9f9c7a212aa46c45035924f426dc0a4756a768fed1bce9360769494fb5b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.9 KB (902884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb33ee2e57f3863801826c7d79504e921a6614912a8d53eeaf2b4cb50fd28ed`

```dockerfile
```

-	Layers:
	-	`sha256:fe877d48bf0383d36a6e9a4c748f248a6693e0372ce795dca8de62f74fe40901`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 890.7 KB (890700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a54e9f623d7bab0bfaf912f22c97e7b7fe62dabd50ede130e38fb44744c8d4`  
		Last Modified: Wed, 28 Jan 2026 03:47:25 GMT  
		Size: 12.2 KB (12184 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e02f8290c02fc3e94800796d754c7e1ced72303591561c957ca0165f1d0fc284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.4 MB (333444789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645ececb909464674722f1339d3605a043babf0b46449c119a99ffe22b180eb9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:54:03 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 28 Jan 2026 03:54:03 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 28 Jan 2026 03:54:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Wed, 28 Jan 2026 03:54:20 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8abb34761bfae0e3d57b55740444b1c0b31ada5127e8cba6452f6602d67aec9`  
		Last Modified: Wed, 28 Jan 2026 03:54:56 GMT  
		Size: 55.6 MB (55558438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b708726fa83464a99ec37220f49eaa3c46df30e5e528119ba7dbe47774a2df`  
		Last Modified: Wed, 28 Jan 2026 03:55:00 GMT  
		Size: 273.8 MB (273796393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:3d07de7b4bdf805a5c04fa49fb1cace9c85193c51baff55c73371e25343d5479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **938.7 KB (938725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15492de8cc191d899d80a79d7acd14274912311d92d7ca5273d25c67d494bb5`

```dockerfile
```

-	Layers:
	-	`sha256:e4f8338aa61f164d8baea6acc8904110a02b63aca7bfe587380c48d16c557eb6`  
		Last Modified: Wed, 28 Jan 2026 03:54:54 GMT  
		Size: 926.4 KB (926420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406a8974c3a43181ea2b31d8db3b02fb7218e7d400ec40c37fc1bfdb40755b7b`  
		Last Modified: Wed, 28 Jan 2026 03:54:54 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:34ead442c42c56225175f8026e623562556b448f5a6a0d35575730fd882c77e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352563196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013c9748d944f33ef7a442735924a764be521d304bf65b38e2af569c66272620`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.20.9-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 05:44:36 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 28 Jan 2026 05:44:36 GMT
RUN apk add --no-cache         ca-certificates         musl-dev         gcc # buildkit
# Wed, 28 Jan 2026 05:44:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.93.0
# Wed, 28 Jan 2026 05:45:02 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3990151ce2a342ec7b501891daf9b442e02873f6a48f096b1bb8bfb26bea6ff2`  
		Last Modified: Wed, 28 Jan 2026 01:18:27 GMT  
		Size: 3.6 MB (3577510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68f09f9ef35077a697b40b8eb052e5985f9c4294c56872d57357e6bc303b94`  
		Last Modified: Wed, 28 Jan 2026 05:46:14 GMT  
		Size: 56.6 MB (56619540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af11aee645b76d3194f79491ff1e8e29262aa4f9a3cc321832b8d202f270e1de`  
		Last Modified: Wed, 28 Jan 2026 05:46:19 GMT  
		Size: 292.4 MB (292366146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:35f653fea4ab54a4b74e232c381b5443faa99c54eedbadfede9004395fff1483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.8 KB (896800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a343514b379df884264799c5ece2aa1877bcf2abf66bd44ea1f2e99fb6f3487`

```dockerfile
```

-	Layers:
	-	`sha256:59cd65e6e8b43f5250daf6306767ab618f5bc332368358d81a3ae60c58e67bd7`  
		Last Modified: Wed, 28 Jan 2026 05:46:11 GMT  
		Size: 884.6 KB (884568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e010517072641bc028341dfad1b8c9e3639606fe940afebfa4d9a279e35bf5bc`  
		Last Modified: Wed, 28 Jan 2026 05:46:11 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.in-toto+json
