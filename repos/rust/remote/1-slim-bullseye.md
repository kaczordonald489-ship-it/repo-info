## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:8b53ec0aaa96beebe0236dbbf70e6c43d3dd6a969b76d3abe48cfe4ab173fa7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:acaae0d55dbb8445a085ea010bfef19ee04ed8c614998372c206034347cf3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303748190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581efbed1658de1e8837b57efc2168c1fdd48688edb4a4719647230ab4ecc2fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:02:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 06:02:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 06:02:31 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3bbf679a7662aa6fa0c359a5d2325c9cf796d85b7dee106262711dd137dd2`  
		Last Modified: Tue, 18 Nov 2025 06:34:38 GMT  
		Size: 273.5 MB (273489707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5d5852c2d8a79e30285e45093864e8d016ddd5e2d8d56ffefad245f8ef735926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24edd5c082b5be4c6b64b8040a39bdad6d876c18ed35d3218ba2f5b4a476fc4f`

```dockerfile
```

-	Layers:
	-	`sha256:90c7880635dc41de9f0ed7434ad8d3be05b8add7739f0a0543330047514e348e`  
		Last Modified: Tue, 18 Nov 2025 06:45:20 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f095a519350dbd516ccc1e41589907fda96959352db3d36220db2bb168266de`  
		Last Modified: Tue, 18 Nov 2025 06:45:21 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:26aea6539a3402cba1051e54af19f47963b90120fbb19f7180da62d6f5911ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325808318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d31e018e9ef32d25d5d1de2a4d62089cbd40fbefb9acd44ab3bf21204ff0d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:02:24 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 05:02:24 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 05:02:24 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88c44611659907face8a04b1321cca4e3d69850d45342155d40b8e4ba9fcb9`  
		Last Modified: Tue, 18 Nov 2025 11:51:06 GMT  
		Size: 300.3 MB (300262066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d387bcc839583c0b0d58b84edcc821578502a18cbbaaad21ce5e27e54eb9df37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1432c5081223c046708a9134a7994b34a371574089cbb8bf23f1504bf962f504`

```dockerfile
```

-	Layers:
	-	`sha256:b7dac7156c2f423d9302b745d4cb7af41837a81ff0a653e108b470d200b95816`  
		Last Modified: Tue, 18 Nov 2025 06:45:26 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f71140f42b2bb7ec981f08cf441913762314440b907a65b8941f84ea689c63`  
		Last Modified: Tue, 18 Nov 2025 06:45:26 GMT  
		Size: 12.8 KB (12793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a0fd954f21f95d1fba135f3bda12bee0b8f8e11ef27575643b0a7c44ea44b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264723914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040834ffeda3e4c079b7b37e0813141bb40b13b4118eaa7ba73d00e3400b17c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:48:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 04:48:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 04:48:42 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c3c581a80aed41db9fc867179dd14df3b25a64e289f1f73788958360b63228`  
		Last Modified: Tue, 18 Nov 2025 07:07:31 GMT  
		Size: 236.0 MB (235975449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:38982fd41a6cd46c2995ee86d3713af970c79fbaaa4449ca4cd635bd638d6722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6f52ff357ddf0b7cb8bba20948e569415023dd3594efffc5b17e25df93f9e7`

```dockerfile
```

-	Layers:
	-	`sha256:b87e1a712f5a3db717f08798ae48e74d24ab4475b6f1b71466c69c2195da254d`  
		Last Modified: Tue, 18 Nov 2025 06:45:31 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37207106ff57e2ee8667bb617b90c180b35cfd90f4c1419c4a2b186705cef3ff`  
		Last Modified: Tue, 18 Nov 2025 06:45:31 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:38aee812f33d3ca926346f75f1be41f9e7f6cafe21cf2188c5c850454dd153c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329904261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00375dba76ea5f56d1202d59fe6619db99d73711ccba570c0078902b2146ee52`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:44:23 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Nov 2025 03:44:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.1
# Tue, 18 Nov 2025 03:44:23 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fa92431247d9c62b6c791fca54f16952c598cc5545329b6db7949cb86417c351`  
		Last Modified: Tue, 18 Nov 2025 01:13:18 GMT  
		Size: 31.2 MB (31191554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80e1dda7158b9c84f051cb88ff4036c7d1f1e2a04e0938c632e2eb8ad7c1cfa`  
		Last Modified: Tue, 18 Nov 2025 11:51:06 GMT  
		Size: 298.7 MB (298712707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a7b1b987e186d7dbf675e7312cb308efaa10236ddae9fb4d4a75c73bec4b0178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9229003cea5b9b3b2817f3477d2fa51d1c239749a05429015e28a70c2ba81c25`

```dockerfile
```

-	Layers:
	-	`sha256:2af403206dcde77de468acf3656b7a1aae9f46cf27206b7daa740d28fe9b5f05`  
		Last Modified: Tue, 18 Nov 2025 06:45:36 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e79c961226e7e0a4657d60f3e931d8588103798fb7d0508c5eef51e0122851`  
		Last Modified: Tue, 18 Nov 2025 06:45:36 GMT  
		Size: 12.7 KB (12681 bytes)  
		MIME: application/vnd.in-toto+json
