## `rust:1-slim`

```console
$ docker pull rust@sha256:5218a2b4b4cb172f26503ac2b2de8e5ffd629ae1c0d885aff2cbe97fd4d1a409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:91c28398f90d64a517804ce27edf32a4ead89895ad0632c2ca6b279369235840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.5 MB (318529923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7eb1e60e744fef7c93fd4cb95b885af859172ba82ca5f817b0bab915d29b66`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:03:54 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 06:03:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 06:03:54 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174ac5060d6d43f5c2ee60c2ca16a7d08c829fc032f8e038bf840a882b189202`  
		Last Modified: Tue, 18 Nov 2025 06:46:18 GMT  
		Size: 288.8 MB (288753439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:82791bfa1387bc32f10e54d98bacf873b2264b282cb19e2817e91ccb2be25c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d79fa8b21d3401526d80753fd2372c43326be0bd30ea1f0a284c8b6e98b509`

```dockerfile
```

-	Layers:
	-	`sha256:4f12bf939de6ca5a4b710a97ced3cb311ce50c2a7d5e0e9da0fb654b77477e35`  
		Last Modified: Tue, 18 Nov 2025 06:44:54 GMT  
		Size: 4.2 MB (4165005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0daeb52ec0041dc08cc627bcc0bbb51afe678db0df9d1afecc678b8a40a51395`  
		Last Modified: Tue, 18 Nov 2025 06:44:56 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:29cf382b68e79c27044d398fae0c3a7388e4e85860c3e36a13efc9d096b01046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334472767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da25a7c3574d9d844ef7e3d582ff98e4e5e60e5cde61808a79f61fa046edd09a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:02:41 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 05:02:41 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 05:02:41 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a3feeeb6326d3dcc3d82223b4ff37abd31a984694108667eaabfe6d8e99e7b`  
		Last Modified: Tue, 18 Nov 2025 07:24:54 GMT  
		Size: 308.3 MB (308262807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:042d3bf0f9efb5bc1da45fb9c07da0a508690b70e597e2dd9f7ea07a2a716ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddba186531a6760416698e6b316c8e8cd56bb9184765227ff859ae31218a6f2`

```dockerfile
```

-	Layers:
	-	`sha256:81cbb9aca0ac27b4e427acfbfcb2329489bbaf25d9b99a9189337cc869b2579e`  
		Last Modified: Tue, 18 Nov 2025 06:45:00 GMT  
		Size: 4.0 MB (3969881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca8e0417e5b0c72f0ef4811a1560eacb66f2ddb85d171f49a1ac7d5625645ca`  
		Last Modified: Tue, 18 Nov 2025 06:45:01 GMT  
		Size: 15.7 KB (15745 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c3b072b144cc7c2349dc3def4b61c0d898147ca03460417cba20a3208374e466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280077365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2443a37981daaa88339d86f8d779275d3eca2d6f4505d7556bc656e5a4f41cfb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:49:16 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 04:49:16 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 04:49:16 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febf7d657eb76b0619d9a73f742ccaab306ba8d26fb6356cf53b0ec6b374873`  
		Last Modified: Tue, 18 Nov 2025 06:46:24 GMT  
		Size: 249.9 MB (249938755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cc45f97e197b30e51e8ff00d5bdf93909bb6543243324dd351a9ff3887668f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42546babf723a924577edd0e9fbcb8ad46b44122fa496768da8c2274cb8eda17`

```dockerfile
```

-	Layers:
	-	`sha256:42c5e81f3800523e05e87699b7c3147c55dae3cfefe72cc5021863a3a5505a6d`  
		Last Modified: Tue, 18 Nov 2025 06:45:05 GMT  
		Size: 4.3 MB (4256221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07fe159e7459375fe2e54a4965a8503ebb6e75b95da7adc61220d4a40cbc7d57`  
		Last Modified: Tue, 18 Nov 2025 06:45:06 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:4211e9afaaa1d2e7f5a946a7c52f0aeec46c3f7ca80a62e321bc3e51084f3e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341732329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ae179dcf37a2a5e1ef26c939a986e781049945e1321f0c49493fc2f93f35b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:44:27 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 03:44:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 03:44:27 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cdac6c22e413331df692c0f1960fe99da067fafc0ae8ed8f8fc0172c4c93f2`  
		Last Modified: Tue, 18 Nov 2025 07:24:51 GMT  
		Size: 310.4 MB (310439261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9166c8b496a35ab1f3cc443ac2ba243159e3be651d67fa26a486f4ecdec4fdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251537c2dfc2bffbbcc29fa24aa9e39fa58976a47edb57759340ab743004b317`

```dockerfile
```

-	Layers:
	-	`sha256:13115356b7afe35c9ff0c36387db03e4f3f3a0472b0203bd2ea2c5715df9d9ae`  
		Last Modified: Tue, 18 Nov 2025 06:45:10 GMT  
		Size: 4.1 MB (4138518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1af918e1564ad3e9e916730a9e89437749684cf8d7400aaf43e79dc292ab948`  
		Last Modified: Tue, 18 Nov 2025 06:45:12 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:5fba22baec74a557819f845926775fc914bf4ee1748f61f5135e4a64bfff9a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395431782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de564ebbe5c666d41394eb8b018ad1014407da26f62ca92a1020b8f5aba529b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:59:03 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 19 Nov 2025 00:59:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Wed, 19 Nov 2025 00:59:03 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7114954665eb2f5a3fffba9c7eacfd12b2a0ca53789ccb22d4c0cf93559607`  
		Last Modified: Wed, 19 Nov 2025 03:55:16 GMT  
		Size: 361.8 MB (361834924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b8c72866ce9633d7e6b518fcbb6b8ed9ac2008b90b264f974558ea414da4623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d831375bd6c16b2cc9509f9f7312dc588b11d7c77d9dc13224d3947202f97f`

```dockerfile
```

-	Layers:
	-	`sha256:9d6493ae3893c006ec137e501fe6c09819d0a07158d1110a34b2391fd6e53eb5`  
		Last Modified: Wed, 19 Nov 2025 03:44:50 GMT  
		Size: 4.2 MB (4161466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092b9717265cb80852418aea12ce891794b83de76b859b85379df4c247c266ab`  
		Last Modified: Wed, 19 Nov 2025 03:44:51 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; riscv64

```console
$ docker pull rust@sha256:6ab23da2d2840a52eaccda1d12c12fb5daa8d8ad82f4327f522dc1b23e1bf454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391685759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4199ee2f4974b0896611dc5c2d53485ed69416671680e5fbb2c39efaaefcc96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:39:10 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 20 Nov 2025 17:39:10 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Thu, 20 Nov 2025 17:39:10 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2842575775c712ee27c2e4a371ee0b6e4aa923279447a249f88624a5aad6c4`  
		Last Modified: Thu, 20 Nov 2025 19:11:58 GMT  
		Size: 363.4 MB (363412633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d742faad984c3f578b522d4ceaf2fd1cf445acde248d4c23342141bcb35f7e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b94380517e22addc0abc4f5470d14a6eb37586d7586fb112fb0d4181aab0b09`

```dockerfile
```

-	Layers:
	-	`sha256:78f496526056e591d6d002620054a9f185880c53e3c2a0c63777a6f3213d698f`  
		Last Modified: Thu, 20 Nov 2025 18:44:42 GMT  
		Size: 4.2 MB (4239422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8054119ec858af0e52188c38633ecff1f386b8e6d67f3c0718a2863e6d3cecf`  
		Last Modified: Thu, 20 Nov 2025 18:44:43 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:5db7d2410b408d2d4cec36f9a9339e319afc80b974c4ab5f2fb6b6e151da497c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379097310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca1f952c23c2645ef7353fff82ae6f0258e94e8026a83bb1700886020a27d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:20:58 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 05:20:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 05:20:58 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2972f3a312260f0850ac686de75bd30ef3c867ddeb9758a4333a146dbb5482`  
		Last Modified: Tue, 18 Nov 2025 07:25:01 GMT  
		Size: 349.3 MB (349262938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e6690ddd92a8d3d205fde2c5fbb965102cd64449b733c4b4300c75061c6d651b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db23a582526fcdd2be112e2481516fa44e20ccd7f1f52afd22cf7355034f8a0`

```dockerfile
```

-	Layers:
	-	`sha256:326177d7b0a70b8c79fa70caa5a83ce234315327341be47059a2b944deed3252`  
		Last Modified: Tue, 18 Nov 2025 06:45:23 GMT  
		Size: 4.0 MB (3982753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f31c6d18b49a24538235d1d1ec7fbac07467ea6c60a7e8f833250f5f1d22c0`  
		Last Modified: Tue, 18 Nov 2025 06:45:24 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json
