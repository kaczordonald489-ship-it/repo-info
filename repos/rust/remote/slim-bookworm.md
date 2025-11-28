## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:c4064394276a4afc5d80928d35b8e158936ab0267cc89fc6dd4c51a14863a71b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:d76f98e31eab65087b839348891048b82943bb9bc825f3129544962ace1b1a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312326873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a90f03a4552e97898ac7b80d905cbca50122aaaab34f50357f8c53c39271a9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:02:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 06:02:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 06:02:49 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dec0101caa276b45af3ff421dfc4d82ec1182306f1226bcfe5e5aea2f5395e8`  
		Last Modified: Tue, 18 Nov 2025 06:48:08 GMT  
		Size: 284.1 MB (284098424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:188258460fb2c01e617619900e9f1d6ee2a1c613ccba67bf364f50d9f1dce4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4109363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab057eacd51f489872c0ee79df3d5e6de9018532def6f226a656cb20e2f789d`

```dockerfile
```

-	Layers:
	-	`sha256:46b84c7aa8438f3b386dd78762b642effdd63bbee1b83b49a3f351c60ef126e0`  
		Last Modified: Tue, 18 Nov 2025 06:45:10 GMT  
		Size: 4.1 MB (4095479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfe07712be57a2d1ad05530935272256995d5ebeee437a61e06e0d39d806881`  
		Last Modified: Tue, 18 Nov 2025 06:45:11 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b451bd9d268266e1e7d1466b08fd53d508c96d5328fd4dc288f568bea68ca6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329763895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018ee2b491559dcd506929baf63c8b61d05ed62f7d423fd286d997bef2e80d26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:02:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 05:02:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 05:02:27 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:56c31a75d861775217bba58452ad642136804e02ff927a701d20990b4efd6793`  
		Last Modified: Tue, 18 Nov 2025 01:13:27 GMT  
		Size: 23.9 MB (23934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d60f84ca932f06eb81542f705955a2c1ffd029023885d70b6f2f38d2bf56a8`  
		Last Modified: Tue, 18 Nov 2025 07:02:33 GMT  
		Size: 305.8 MB (305829886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:702cc65e10869ff220e1e566607d9e320895a76964cc45ad0a3a08e0d3cbf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0fd3f3c00e225b0809ada0eefd4888c45bbb6d2a9d6436994f186299a176c5`

```dockerfile
```

-	Layers:
	-	`sha256:09bb863a714948ce0122b069874758969ea1332e67c447a5985f7d575d8476ae`  
		Last Modified: Tue, 18 Nov 2025 06:45:15 GMT  
		Size: 3.9 MB (3909876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c07de61f8cbaf10f65a471789059d0f8110f226fb6710f50b168a908906a26a`  
		Last Modified: Tue, 18 Nov 2025 06:45:16 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e5a5c68ee4b8dcb856b2ca08710a0768d21db34bd55737e8572b22d455a15064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274224622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53929c4086859e433a1a9eacb64a2a30ec40d0f4048afececdd130bd478d44b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:49:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 04:49:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 04:49:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7888374cc628c98d74f2d5ddff405e31672751c1a9d58bfe56729e30734a283d`  
		Last Modified: Tue, 18 Nov 2025 06:47:29 GMT  
		Size: 246.1 MB (246122415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c812a5c0bd9c939a83258a7d3b7746c914c8f05946ffc938249bf1ebdb0fc78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c43d1c76b0d40ea85dc13d1eca058700cbc968cc93dca5eec9be586ebe202c`

```dockerfile
```

-	Layers:
	-	`sha256:63c6d6c5c5a88329732d7e3f68a12e05c8fcda7ae4854d6e234886a62a2a4825`  
		Last Modified: Tue, 18 Nov 2025 06:45:21 GMT  
		Size: 4.1 MB (4117775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d46eae406f582630e63d16772184d0ae99f5411bf8a37af81230e543662d47`  
		Last Modified: Tue, 18 Nov 2025 06:45:21 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bf89b5568fad31d1400538a525838b461cfa499a6ac6c12456e356ce7303f297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334753296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ce05f3bdf1f8d43ed34f4f85acbcf714d057c7b5d27f19fdc3012db41dd86b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:44:23 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 03:44:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 03:44:23 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a2d00ea50374d5273894aeb64d33be9c21e677e44d789c4db64af25f578b3`  
		Last Modified: Tue, 18 Nov 2025 07:03:30 GMT  
		Size: 305.5 MB (305543592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:35c88aa443be7cce5f45b55fee0171e592896a2d14e192a62e2a93ea0fbd4c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b75350f2cbc0f6e3ecd05307ae24608b9fb17bd23f20bb19d47442e072876ba`

```dockerfile
```

-	Layers:
	-	`sha256:742c9e1e99f9e0b4829b45130f3473ef141889cec860bffb4933fd520262d02c`  
		Last Modified: Tue, 18 Nov 2025 06:45:25 GMT  
		Size: 4.1 MB (4074862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a823614f5fa21cb01d1993682a2f49a044f5be6dc65eaebd16151e9e8b24b7ac`  
		Last Modified: Tue, 18 Nov 2025 06:45:26 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:6c96263265ad735c1902e8a329a461d1f782c4dc131df1e0f59cd9c9392bf328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 MB (395795144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98bc3ee7ae36ea2e6448fda9744d0e1081fe8c3963290cdebc4ba807b2dd534`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:08:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 06:08:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 06:08:13 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032ac1e78f094b09de1fcf185cc72bb5608fdf6bcabad2e8571b6eade1edeba7`  
		Last Modified: Tue, 18 Nov 2025 07:06:20 GMT  
		Size: 363.7 MB (363726318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:27e3d7f63b5938eaf79d3661aef163507c24a434cf95713cf373b61f77e5147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9cd4d52fb241d25e3333a1c0ced065ec997e5cb4f30250475468209f625737`

```dockerfile
```

-	Layers:
	-	`sha256:81b49458846a049e6b71e2b2143751da58a81fb50012bdba1f4c72df93855c86`  
		Last Modified: Tue, 18 Nov 2025 06:45:30 GMT  
		Size: 4.1 MB (4069081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73522220365a50e6a92d5144de9a090335eab21ce1b9044cff1a565fdebf5548`  
		Last Modified: Tue, 18 Nov 2025 06:45:31 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b404899f78c7c43fc815c80e6bb475cddffa829e1a4966d46eaf417bd4f2d7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373923181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb81bb9e45c110d11fefca6eb410762bc647d105e1a375aac3f008eecea42a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:20:58 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 05:20:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 05:20:58 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c0af292970613baf44599c23d2133e4d6c4525f6a6f26de8fd8bfe8f4de499`  
		Last Modified: Tue, 18 Nov 2025 07:06:40 GMT  
		Size: 347.0 MB (347038789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:502d13a66ec2d658b68d85e385c390ad52f95137a82d37f935f000c23a23dbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0692130c577fffbc24c81bbcea4233273e6b2954aeeff1eb0def12fc407849`

```dockerfile
```

-	Layers:
	-	`sha256:053560db093d952a0f7c6a8cdf921081c794193ed24ebbc0937f537f638a2958`  
		Last Modified: Tue, 18 Nov 2025 06:45:35 GMT  
		Size: 3.9 MB (3933157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5077bc72975aacf2080b2428019fd3ad283fd6b031b1d7c17f3b00189cda684`  
		Last Modified: Tue, 18 Nov 2025 06:45:36 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json
