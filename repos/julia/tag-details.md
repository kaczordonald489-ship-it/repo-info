<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-trixie`](#julia1-trixie)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1-windowsservercore-ltsc2025`](#julia1-windowsservercore-ltsc2025)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.21`](#julia110-alpine321)
-	[`julia:1.10-alpine3.22`](#julia110-alpine322)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-trixie`](#julia110-trixie)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10-windowsservercore-ltsc2025`](#julia110-windowsservercore-ltsc2025)
-	[`julia:1.10.10`](#julia11010)
-	[`julia:1.10.10-alpine`](#julia11010-alpine)
-	[`julia:1.10.10-alpine3.21`](#julia11010-alpine321)
-	[`julia:1.10.10-alpine3.22`](#julia11010-alpine322)
-	[`julia:1.10.10-bookworm`](#julia11010-bookworm)
-	[`julia:1.10.10-trixie`](#julia11010-trixie)
-	[`julia:1.10.10-windowsservercore`](#julia11010-windowsservercore)
-	[`julia:1.10.10-windowsservercore-ltsc2022`](#julia11010-windowsservercore-ltsc2022)
-	[`julia:1.10.10-windowsservercore-ltsc2025`](#julia11010-windowsservercore-ltsc2025)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-trixie`](#julia111-trixie)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11-windowsservercore-ltsc2025`](#julia111-windowsservercore-ltsc2025)
-	[`julia:1.11.7`](#julia1117)
-	[`julia:1.11.7-bookworm`](#julia1117-bookworm)
-	[`julia:1.11.7-trixie`](#julia1117-trixie)
-	[`julia:1.11.7-windowsservercore`](#julia1117-windowsservercore)
-	[`julia:1.11.7-windowsservercore-ltsc2022`](#julia1117-windowsservercore-ltsc2022)
-	[`julia:1.11.7-windowsservercore-ltsc2025`](#julia1117-windowsservercore-ltsc2025)
-	[`julia:1.12`](#julia112)
-	[`julia:1.12-bookworm`](#julia112-bookworm)
-	[`julia:1.12-trixie`](#julia112-trixie)
-	[`julia:1.12-windowsservercore`](#julia112-windowsservercore)
-	[`julia:1.12-windowsservercore-ltsc2022`](#julia112-windowsservercore-ltsc2022)
-	[`julia:1.12-windowsservercore-ltsc2025`](#julia112-windowsservercore-ltsc2025)
-	[`julia:1.12.2`](#julia1122)
-	[`julia:1.12.2-bookworm`](#julia1122-bookworm)
-	[`julia:1.12.2-trixie`](#julia1122-trixie)
-	[`julia:1.12.2-windowsservercore`](#julia1122-windowsservercore)
-	[`julia:1.12.2-windowsservercore-ltsc2022`](#julia1122-windowsservercore-ltsc2022)
-	[`julia:1.12.2-windowsservercore-ltsc2025`](#julia1122-windowsservercore-ltsc2025)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:latest`](#julialatest)
-	[`julia:trixie`](#juliatrixie)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)
-	[`julia:windowsservercore-ltsc2025`](#juliawindowsservercore-ltsc2025)

## `julia:1`

```console
$ docker pull julia@sha256:854de5495d7a932103bb164923ea40441ee2f7e2c95f2eb7edac6a0f81eeb1e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:0feea4981d0f0b0ef007df377a3afac39c6fbcdc0b509330c789376a60a8b3a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:ebd943bccbcb194f9d5f0bb771d1064f124995ede9bc90baf866d62a06ac0cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323892306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea21809e86116583b0d88dfa11d5f5b9b4204351012c09219670025116e98d0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:38:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede5ccf9c6259cfc06511259b60c6ac73ba7f2fe6a4fc52f629ead8f70a1137b`  
		Last Modified: Mon, 24 Nov 2025 22:39:58 GMT  
		Size: 5.7 MB (5716408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f681efbbc76aebdf3eea9d90ede7a11f9d56bf62c6604abaacfe8f572ef1dc`  
		Last Modified: Tue, 25 Nov 2025 00:17:15 GMT  
		Size: 289.9 MB (289947080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20c522aa2e3a84dd11ed978edfd648fd25db01e32b9239f9534d62c1b5b6e6b`  
		Last Modified: Mon, 24 Nov 2025 22:39:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3ef845e7f11dc238ebe4eb7f322e328fda60575f7646774abbccff44f1360da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd24da63876208897d7ff6207bd15c671cedbdd26e453242baf5db8046deef90`

```dockerfile
```

-	Layers:
	-	`sha256:0ebb24515878f7357c14bdbff5a2548fbb94661e40603ca0ffb4e02c111a194a`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc92f28800b448530c7176f4f615cb2258c03bf1e94bbeb1731e00658a1ef67c`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3dfc6b09e66f688b9901969cab733eadaa7e456bcad3c4cecee5e297e6072fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344622258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9e2abe7468fc884efc51e7726c46898d3f2e934faa2f5d11f661cf4700a94a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:39:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560374fb6f10760919cfedfebbba3b0f6ec46de28729df786cba4c8fc3fdd7bb`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 5.6 MB (5567216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850889d615ff2706ab9dcd96187e71512e172e8717102b5c174265725c2098b7`  
		Last Modified: Tue, 25 Nov 2025 00:17:47 GMT  
		Size: 311.0 MB (310952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e26358d6614ef2e86eb4e97171e43030aa04c143e5d26e34d63c20b4873d42`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:abfa0f12c098fa7adff539a01c0ccfa25a52b1ca703b39eaac97ccd872d3b72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88acdcedeb7569b9be9bf9022215da5e51daef9e7fe15a146ad685467cb07923`

```dockerfile
```

-	Layers:
	-	`sha256:8fb1bdaf1f81e85bb42847721687590cccea14a6a68f2f31636b44bbff262e87`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ad70d36ab4a56fa2a3bc6d3bc715247173fdf1f572003787265991ef8de6a3`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:f755775da5f3613be0b4655c9d19a72c4208776e2af4dafe26f51ea85a639f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266222757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a22b792e310d5f7def5af8d56e49eaa65335bd523a826b14c2394ff0d581f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd7b893f16d80738b2e0d480c2c48dcc9a045a3df6d084caf564d380eba3588`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 5.9 MB (5877997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b706a608f58d09d21fca9473fa23c5a70796cfd9eab3f397ab722205461fa6a`  
		Last Modified: Tue, 25 Nov 2025 00:16:56 GMT  
		Size: 231.1 MB (231134686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f76d01befd1d4895eb64055e752e8d64d28b21b10ef46110f60b17c84a7290`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3801140c193396ba8c6c7c3d7dec41496528dce0744a1a511936c7bfe3ec341f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cc08585cd4984bc999ff1276105e3c4c35776821144b00e3f2401d932cb206`

```dockerfile
```

-	Layers:
	-	`sha256:851a3ee9b0a8eaf1dc0fc439a91f4a546435d070254ba43d269e7f86405cd9be`  
		Last Modified: Tue, 25 Nov 2025 00:02:46 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b279851a6615b5c52a4c4c6da944b3681413b200a24becb1add45bd2d3bdad4`  
		Last Modified: Tue, 25 Nov 2025 00:02:47 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-trixie`

```console
$ docker pull julia@sha256:d3dc1f6f39a492829c6e74eaa2a26f68d3dcba577b1ddae9960f83ad4626d9b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-trixie` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:11aee8627b47e4ed5e908a587ae55c98c86ccd8117f65566a96f1ee0ddf742b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:543d2532e513d8a1a42648f9dc78c42b9ce1a8a2d68676b185fbd36c75ec2dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:ec852fdf68ade5279f9b5ef65a1833e073d343f9bc224b63bf1caabcd4a9e38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:4e047cb3a84a0b25ccd2e4eea947a4c60f699516eb7124b210f47f125ce37185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:0fe1fe2efc1bbe1224c58a4734af34edf3d046588f56ecd7ec4f34a99a854d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195667667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031c9ff6deb5506659633fb5eb723d0d5ddc19c189864bb8fad99310ac44ffdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:08:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 15:08:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:08:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca5873c25d95e4a8277a7214ee4210f194515f6dcfb85c65961ac922a19f76`  
		Last Modified: Tue, 18 Nov 2025 15:30:16 GMT  
		Size: 155.4 MB (155388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9991c334a121617ade33f937d2f8399e321ea54d0ffc59e5b3f732078c09542`  
		Last Modified: Tue, 18 Nov 2025 15:09:09 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:f894cd8fc71d8b1e87b111f5ad34546ed48acca923b81d422aae48f5df7d98eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75906a43119a64a1f18b9ac13a72fc32af0f845c6a57f4791a457484b1283e9`

```dockerfile
```

-	Layers:
	-	`sha256:c7351c68480fb54a08d763a82bc7665187b6d9316ee09826fce4b163b1f4564c`  
		Last Modified: Tue, 18 Nov 2025 18:02:49 GMT  
		Size: 2.2 MB (2242678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9005dd48343b02c2fb0f41e0dc7d7d4c84f69326337994f827335c8216640bab`  
		Last Modified: Tue, 18 Nov 2025 18:02:50 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.21`

```console
$ docker pull julia@sha256:d1a3e070ace2a47e5eb3cf2e507a090c9b0be78e986d61fa40b7b708e53a3842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:52ac97bc4b7d2863b731985c6614a46e6ab4f13f13f3c8d91d933a5c13055102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181941938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df008c40538a112568d8ff3054242fbabee9d18edd7f08445c7c38cf6f7cea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514bda53ebb21b1322cf919f16ba5b28ae9b1d9acd8c0d0da1518623793417c9`  
		Last Modified: Sat, 11 Oct 2025 01:40:30 GMT  
		Size: 178.3 MB (178298998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d772ec346b861be7ae3ae4939fab2ea82732b66bf0931f5d9a7cb217646c0c6`  
		Last Modified: Wed, 08 Oct 2025 23:29:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:9b1b7279a096a1493387b3ed071e6f6201a78ed8dfd3ecc09596e34b48a8e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a9169be517a413e716324eb64afaf1e70b5e4bf29b7ab8205696d41c42cfd`

```dockerfile
```

-	Layers:
	-	`sha256:d87cc8698e0b72551245a2ae783ddb2d064e0bf0c6a2b90e877668ed5777c209`  
		Last Modified: Thu, 09 Oct 2025 02:02:25 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b3221cfc383c0844d2d950de60a17caa749b9d059d4a7e43848dc1f00be791`  
		Last Modified: Thu, 09 Oct 2025 02:02:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.22`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:5381d01c3615422f73fde38e729f1817068c6b5bab9160ba2d98b243b352217f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:299c3c8333df7a50dcd02ebccef345b1f88048f6c7d892001481cd378c5d46cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c18876753015f55ad8389bc1856f4d5d847bfbadb6b3146d0b023332bbeca92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:22:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:22:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be4ab744883e883a44090eab187db08ad07885ee0d0e0a30d296c508fb12ba`  
		Last Modified: Tue, 18 Nov 2025 04:23:25 GMT  
		Size: 5.7 MB (5716399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686df9e4f2726cc605d0bb4489f6b0259b3b543877e935cd58c1183252aa4b21`  
		Last Modified: Tue, 18 Nov 2025 06:11:30 GMT  
		Size: 176.3 MB (176324443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061c64217926f23766909405893cb28a9640e36e487fbc69b8eb50a226575d2`  
		Last Modified: Tue, 18 Nov 2025 04:23:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9174cb7321d5fb61b395fd1388ace0d42af55407c54f50a81b74f66515b9bdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4d25e0e4acc0b84213fc7c5f7bae960ae76aeac5a4ec60332e591ace7ba26`

```dockerfile
```

-	Layers:
	-	`sha256:18a0814e0c9aa4c785962304e74d9d35451f6f8e418467e8091daa6af258b9c7`  
		Last Modified: Tue, 18 Nov 2025 06:03:57 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da5bbba4e084f79beb08d7b46c9429e44212f1262b14763c5f4716f4ae8d715`  
		Last Modified: Tue, 18 Nov 2025 06:03:58 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2f54cb3c7b23e9497c60cacc75eaef83da3df5a0f7fc96e467ad90b141df7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e0059c86daa089e2f731ea3150573f7d79099097ad5c5fd8f31ce915d5c88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:21:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029027c6d63baf7bfb9843abd2fc2b739a48610216f6132b6edae462f0e70734`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 5.6 MB (5567166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9545252869703d4ce0e49fcdf41cd588fe96835981a05369a36ce986020e28c`  
		Last Modified: Tue, 18 Nov 2025 16:03:34 GMT  
		Size: 177.4 MB (177412364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7ef2dadcdb140ad4b9f2b3f3829abe44b958b9a512f807804900d532bb7ae924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4843b55b5922d4066c7f8f3b168bbc1d4c2b89f00a994633d065684b1184026c`

```dockerfile
```

-	Layers:
	-	`sha256:8a6ff17a86147fb1fadaa3a71d31e969243eaf0896367426923006db64cd4b02`  
		Last Modified: Tue, 18 Nov 2025 06:04:01 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7d6fa523d4c3f549df4f16cac0945b6acba055e8e734f97d319f98a42faaa8`  
		Last Modified: Tue, 18 Nov 2025 06:04:02 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:326af20227013fbdd0156b2d2ee43db097484c827fcc3aec43fa4925e4ba3ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192896018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c921fbab4361fcba7d253fc77de5537d5a542f663815c9fbc9a0f6d983ac364e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:42 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddf024a336add7a4bafd65783505344c840e3b64ef41d5a68fc540092ddc09`  
		Last Modified: Tue, 18 Nov 2025 02:18:16 GMT  
		Size: 5.9 MB (5878045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0974eea60241dff1791390f05414a3817f6bbd4defa337d806a4d83166f5e2`  
		Last Modified: Tue, 18 Nov 2025 23:56:46 GMT  
		Size: 157.8 MB (157807896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88776365c66fe4d3148f220baf334f4b674412fe6da649aa9778403dd7134e2`  
		Last Modified: Tue, 18 Nov 2025 02:18:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8a7b9ce85a0ca059b2b718b53460c232e85f29167b9b464206f4b1945cb68a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267488b28cf6c60e10a924367fa711ebd7d55b57a1e4cd95e1c03f8aa2abd084`

```dockerfile
```

-	Layers:
	-	`sha256:575fbafb05234551dc16bb57a360f4bf010103579ab27ba7c970887ca9757627`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f856465ed88fe4eb461f74180038b639c6293359b5861332e985f739c00a8c9b`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:1bf868a2bbd05fc69edbf1e4373833db83eb5b228b46f21c5ed9a53b10413d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b07b177a9c9eae6c41790122e166f51518ff1955d9a6c2869d4fae4781aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:16:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940cffb1d6213886988c4c3af3f5f6a0cc37446b6878a8e2362ae10674c75ca`  
		Last Modified: Tue, 18 Nov 2025 02:16:58 GMT  
		Size: 155.4 MB (155354870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5ed149e466cf636d1d47da92f0c9f90446f713ada2c3166034e0926e10e9c`  
		Last Modified: Tue, 18 Nov 2025 02:17:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:21a1ab46f506a7f4ed9e147dac642116d38a0cbd6ba7f662e90d9e9d11f3e0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4de383be6b49ff52003f8e52872e47baf8d2cb858fb56d1b68d77ecbd3ff2d5`

```dockerfile
```

-	Layers:
	-	`sha256:741d0c0be3f8b98b8d14a923b3453801cce2a243bc99e86a3ab73a1fac526c89`  
		Last Modified: Tue, 18 Nov 2025 06:04:10 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed32c4698b545c221a8efa988a4627102accb5850943951be72ecba9f68334b7`  
		Last Modified: Tue, 18 Nov 2025 06:04:11 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-trixie`

```console
$ docker pull julia@sha256:38ad2479e6e47e6c698470b361251c3bea60f5e41813e203e87c5d9f7347dd85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10-trixie` - linux; amd64

```console
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:0fe1fe2efc1bbe1224c58a4734af34edf3d046588f56ecd7ec4f34a99a854d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195667667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031c9ff6deb5506659633fb5eb723d0d5ddc19c189864bb8fad99310ac44ffdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:08:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 15:08:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:08:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca5873c25d95e4a8277a7214ee4210f194515f6dcfb85c65961ac922a19f76`  
		Last Modified: Tue, 18 Nov 2025 15:30:16 GMT  
		Size: 155.4 MB (155388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9991c334a121617ade33f937d2f8399e321ea54d0ffc59e5b3f732078c09542`  
		Last Modified: Tue, 18 Nov 2025 15:09:09 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f894cd8fc71d8b1e87b111f5ad34546ed48acca923b81d422aae48f5df7d98eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75906a43119a64a1f18b9ac13a72fc32af0f845c6a57f4791a457484b1283e9`

```dockerfile
```

-	Layers:
	-	`sha256:c7351c68480fb54a08d763a82bc7665187b6d9316ee09826fce4b163b1f4564c`  
		Last Modified: Tue, 18 Nov 2025 18:02:49 GMT  
		Size: 2.2 MB (2242678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9005dd48343b02c2fb0f41e0dc7d7d4c84f69326337994f827335c8216640bab`  
		Last Modified: Tue, 18 Nov 2025 18:02:50 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:a2b6f5a6a95d9c683292573eccb843e8b54aa433a6ba14303e729f974db13049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d47e5e780c6d6b04f7050bc6c19aa3ae6d993a5bb47b4192bea88d1cfb0dacda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:f48a86cec5e53df7158d643facd17ae90ac31141e7c1316cbd8a68de962e16a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10`

```console
$ docker pull julia@sha256:4e047cb3a84a0b25ccd2e4eea947a4c60f699516eb7124b210f47f125ce37185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10.10` - linux; amd64

```console
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; ppc64le

```console
$ docker pull julia@sha256:0fe1fe2efc1bbe1224c58a4734af34edf3d046588f56ecd7ec4f34a99a854d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195667667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031c9ff6deb5506659633fb5eb723d0d5ddc19c189864bb8fad99310ac44ffdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:08:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 15:08:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:08:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca5873c25d95e4a8277a7214ee4210f194515f6dcfb85c65961ac922a19f76`  
		Last Modified: Tue, 18 Nov 2025 15:30:16 GMT  
		Size: 155.4 MB (155388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9991c334a121617ade33f937d2f8399e321ea54d0ffc59e5b3f732078c09542`  
		Last Modified: Tue, 18 Nov 2025 15:09:09 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:f894cd8fc71d8b1e87b111f5ad34546ed48acca923b81d422aae48f5df7d98eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75906a43119a64a1f18b9ac13a72fc32af0f845c6a57f4791a457484b1283e9`

```dockerfile
```

-	Layers:
	-	`sha256:c7351c68480fb54a08d763a82bc7665187b6d9316ee09826fce4b163b1f4564c`  
		Last Modified: Tue, 18 Nov 2025 18:02:49 GMT  
		Size: 2.2 MB (2242678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9005dd48343b02c2fb0f41e0dc7d7d4c84f69326337994f827335c8216640bab`  
		Last Modified: Tue, 18 Nov 2025 18:02:50 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-alpine`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.21`

```console
$ docker pull julia@sha256:d1a3e070ace2a47e5eb3cf2e507a090c9b0be78e986d61fa40b7b708e53a3842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:52ac97bc4b7d2863b731985c6614a46e6ab4f13f13f3c8d91d933a5c13055102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181941938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df008c40538a112568d8ff3054242fbabee9d18edd7f08445c7c38cf6f7cea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514bda53ebb21b1322cf919f16ba5b28ae9b1d9acd8c0d0da1518623793417c9`  
		Last Modified: Sat, 11 Oct 2025 01:40:30 GMT  
		Size: 178.3 MB (178298998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d772ec346b861be7ae3ae4939fab2ea82732b66bf0931f5d9a7cb217646c0c6`  
		Last Modified: Wed, 08 Oct 2025 23:29:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:9b1b7279a096a1493387b3ed071e6f6201a78ed8dfd3ecc09596e34b48a8e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a9169be517a413e716324eb64afaf1e70b5e4bf29b7ab8205696d41c42cfd`

```dockerfile
```

-	Layers:
	-	`sha256:d87cc8698e0b72551245a2ae783ddb2d064e0bf0c6a2b90e877668ed5777c209`  
		Last Modified: Thu, 09 Oct 2025 02:02:25 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b3221cfc383c0844d2d950de60a17caa749b9d059d4a7e43848dc1f00be791`  
		Last Modified: Thu, 09 Oct 2025 02:02:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.22`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-bookworm`

```console
$ docker pull julia@sha256:5381d01c3615422f73fde38e729f1817068c6b5bab9160ba2d98b243b352217f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:299c3c8333df7a50dcd02ebccef345b1f88048f6c7d892001481cd378c5d46cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c18876753015f55ad8389bc1856f4d5d847bfbadb6b3146d0b023332bbeca92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:22:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:22:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be4ab744883e883a44090eab187db08ad07885ee0d0e0a30d296c508fb12ba`  
		Last Modified: Tue, 18 Nov 2025 04:23:25 GMT  
		Size: 5.7 MB (5716399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686df9e4f2726cc605d0bb4489f6b0259b3b543877e935cd58c1183252aa4b21`  
		Last Modified: Tue, 18 Nov 2025 06:11:30 GMT  
		Size: 176.3 MB (176324443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061c64217926f23766909405893cb28a9640e36e487fbc69b8eb50a226575d2`  
		Last Modified: Tue, 18 Nov 2025 04:23:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9174cb7321d5fb61b395fd1388ace0d42af55407c54f50a81b74f66515b9bdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4d25e0e4acc0b84213fc7c5f7bae960ae76aeac5a4ec60332e591ace7ba26`

```dockerfile
```

-	Layers:
	-	`sha256:18a0814e0c9aa4c785962304e74d9d35451f6f8e418467e8091daa6af258b9c7`  
		Last Modified: Tue, 18 Nov 2025 06:03:57 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da5bbba4e084f79beb08d7b46c9429e44212f1262b14763c5f4716f4ae8d715`  
		Last Modified: Tue, 18 Nov 2025 06:03:58 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2f54cb3c7b23e9497c60cacc75eaef83da3df5a0f7fc96e467ad90b141df7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e0059c86daa089e2f731ea3150573f7d79099097ad5c5fd8f31ce915d5c88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:21:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029027c6d63baf7bfb9843abd2fc2b739a48610216f6132b6edae462f0e70734`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 5.6 MB (5567166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9545252869703d4ce0e49fcdf41cd588fe96835981a05369a36ce986020e28c`  
		Last Modified: Tue, 18 Nov 2025 16:03:34 GMT  
		Size: 177.4 MB (177412364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7ef2dadcdb140ad4b9f2b3f3829abe44b958b9a512f807804900d532bb7ae924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4843b55b5922d4066c7f8f3b168bbc1d4c2b89f00a994633d065684b1184026c`

```dockerfile
```

-	Layers:
	-	`sha256:8a6ff17a86147fb1fadaa3a71d31e969243eaf0896367426923006db64cd4b02`  
		Last Modified: Tue, 18 Nov 2025 06:04:01 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7d6fa523d4c3f549df4f16cac0945b6acba055e8e734f97d319f98a42faaa8`  
		Last Modified: Tue, 18 Nov 2025 06:04:02 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:326af20227013fbdd0156b2d2ee43db097484c827fcc3aec43fa4925e4ba3ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192896018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c921fbab4361fcba7d253fc77de5537d5a542f663815c9fbc9a0f6d983ac364e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:42 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddf024a336add7a4bafd65783505344c840e3b64ef41d5a68fc540092ddc09`  
		Last Modified: Tue, 18 Nov 2025 02:18:16 GMT  
		Size: 5.9 MB (5878045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0974eea60241dff1791390f05414a3817f6bbd4defa337d806a4d83166f5e2`  
		Last Modified: Tue, 18 Nov 2025 23:56:46 GMT  
		Size: 157.8 MB (157807896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88776365c66fe4d3148f220baf334f4b674412fe6da649aa9778403dd7134e2`  
		Last Modified: Tue, 18 Nov 2025 02:18:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8a7b9ce85a0ca059b2b718b53460c232e85f29167b9b464206f4b1945cb68a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267488b28cf6c60e10a924367fa711ebd7d55b57a1e4cd95e1c03f8aa2abd084`

```dockerfile
```

-	Layers:
	-	`sha256:575fbafb05234551dc16bb57a360f4bf010103579ab27ba7c970887ca9757627`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f856465ed88fe4eb461f74180038b639c6293359b5861332e985f739c00a8c9b`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:1bf868a2bbd05fc69edbf1e4373833db83eb5b228b46f21c5ed9a53b10413d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b07b177a9c9eae6c41790122e166f51518ff1955d9a6c2869d4fae4781aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:16:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940cffb1d6213886988c4c3af3f5f6a0cc37446b6878a8e2362ae10674c75ca`  
		Last Modified: Tue, 18 Nov 2025 02:16:58 GMT  
		Size: 155.4 MB (155354870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5ed149e466cf636d1d47da92f0c9f90446f713ada2c3166034e0926e10e9c`  
		Last Modified: Tue, 18 Nov 2025 02:17:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:21a1ab46f506a7f4ed9e147dac642116d38a0cbd6ba7f662e90d9e9d11f3e0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4de383be6b49ff52003f8e52872e47baf8d2cb858fb56d1b68d77ecbd3ff2d5`

```dockerfile
```

-	Layers:
	-	`sha256:741d0c0be3f8b98b8d14a923b3453801cce2a243bc99e86a3ab73a1fac526c89`  
		Last Modified: Tue, 18 Nov 2025 06:04:10 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed32c4698b545c221a8efa988a4627102accb5850943951be72ecba9f68334b7`  
		Last Modified: Tue, 18 Nov 2025 06:04:11 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-trixie`

```console
$ docker pull julia@sha256:38ad2479e6e47e6c698470b361251c3bea60f5e41813e203e87c5d9f7347dd85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10.10-trixie` - linux; amd64

```console
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:0fe1fe2efc1bbe1224c58a4734af34edf3d046588f56ecd7ec4f34a99a854d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195667667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031c9ff6deb5506659633fb5eb723d0d5ddc19c189864bb8fad99310ac44ffdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:08:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:08:07 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 15:08:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:08:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca5873c25d95e4a8277a7214ee4210f194515f6dcfb85c65961ac922a19f76`  
		Last Modified: Tue, 18 Nov 2025 15:30:16 GMT  
		Size: 155.4 MB (155388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9991c334a121617ade33f937d2f8399e321ea54d0ffc59e5b3f732078c09542`  
		Last Modified: Tue, 18 Nov 2025 15:09:09 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f894cd8fc71d8b1e87b111f5ad34546ed48acca923b81d422aae48f5df7d98eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75906a43119a64a1f18b9ac13a72fc32af0f845c6a57f4791a457484b1283e9`

```dockerfile
```

-	Layers:
	-	`sha256:c7351c68480fb54a08d763a82bc7665187b6d9316ee09826fce4b163b1f4564c`  
		Last Modified: Tue, 18 Nov 2025 18:02:49 GMT  
		Size: 2.2 MB (2242678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9005dd48343b02c2fb0f41e0dc7d7d4c84f69326337994f827335c8216640bab`  
		Last Modified: Tue, 18 Nov 2025 18:02:50 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-windowsservercore`

```console
$ docker pull julia@sha256:a2b6f5a6a95d9c683292573eccb843e8b54aa433a6ba14303e729f974db13049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10.10-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d47e5e780c6d6b04f7050bc6c19aa3ae6d993a5bb47b4192bea88d1cfb0dacda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:f48a86cec5e53df7158d643facd17ae90ac31141e7c1316cbd8a68de962e16a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.10.10-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:7296f7aa7ceecef50a64b34d55a95cdbdd86c7bb6c4f6dc4388e56f0181862bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 17:26:49 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Mon, 24 Nov 2025 04:21:22 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:6f9c2697e2a79bbb1ec77021b95238ed8a985a721748be7c4feb75cdb6424554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288855432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726b2c2f668e59b9ff7c1cc557ee81df169c5e608745b3b02e023c5e0d5cd538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:06:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 15:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:06:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb0ca605c9a4aa95330b7c16cb77d9773f3b80c4f94ee7019d057b54beaef0`  
		Last Modified: Tue, 18 Nov 2025 15:29:23 GMT  
		Size: 248.6 MB (248576032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf08d0a5c00f2c1f3ebd27f9cfa445162205a3c1e43d743b7a5610aec7c6742d`  
		Last Modified: Tue, 18 Nov 2025 15:08:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:592022e028c33e123281e031ca402bd1c920527d13752917b2a7d91a87bbd015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d469d9a4fd37934de0e7dacc608325aab02b88755e3e1750cd62aeb77968f7`

```dockerfile
```

-	Layers:
	-	`sha256:287af6c7630ed30d8e049560096bd452d5ca779fbb55a139181fce6f4b0d3aa1`  
		Last Modified: Tue, 18 Nov 2025 18:03:17 GMT  
		Size: 2.2 MB (2242674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69767a5e8bcd89c2bc3f71bceaced409601de9818a84d4716698fa787a816e0f`  
		Last Modified: Tue, 18 Nov 2025 18:03:19 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:8b0ad8e6d29ed3767dcbc838f778c1f092fd68b9f7f4ff9060ee3fac461c9269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:f4d3fac0fa62fb597cc498694fb26973346b837b9d14926dc8d5f6fc17d32c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c242212b04129672d2d70409ef0274ed477a2612e5db3c901967ea10d61ae11e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:21:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64287521fae1ed74e55d6db247c476f376f6326d8692b926ddaff00d264660e`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 5.7 MB (5716403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a695f03af55a8be1b1c5d34345a35e3f2d95d1ae0ce06fd24a16c32d0016110`  
		Last Modified: Tue, 18 Nov 2025 07:26:54 GMT  
		Size: 288.8 MB (288788343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4ab0dafaefcf335596cd20cdb877acd34f9746b8f0b69cc01f3f359b964eff`  
		Last Modified: Tue, 18 Nov 2025 04:22:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:93247f777bb0a6004b5af30109be1404066ebbce81229f9e8ccccb23ac61f450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc357a4f5c3b5ecb668442c6af292c7fa41801319ad9ba7489242ce108260aa8`

```dockerfile
```

-	Layers:
	-	`sha256:af0a12fa1bbaf70991bc885de8a505ad526520a0328a2ef2a64769262d6c565e`  
		Last Modified: Tue, 18 Nov 2025 06:04:34 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba641224ecb950287995cc172d09e26d07e19ad4ba0255e4ca5308125df15002`  
		Last Modified: Tue, 18 Nov 2025 06:04:35 GMT  
		Size: 16.6 KB (16583 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:919245c9db92ef7b659033cc127763743edc8ca281c0e225d0dcb2d9d8e89d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c9d30335a960582fb6e9f651d35c90d160ec47e42868e7f228fa83132cc743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18288eecc7d13e180b657797c35b3effcf06ed2ebd361ab629425ebc62a7bab8`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 5.6 MB (5567234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac828501f908b9f48f5885eadac374ee7f922484e46f80bc0c6ee521c97f0b0d`  
		Last Modified: Tue, 18 Nov 2025 15:58:28 GMT  
		Size: 304.6 MB (304646684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f5a7472d204b48f1950002bbd423e6cb2e6289962ce1c0f3c1df7c1006d92`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9c8015ebeb6a0e77e23f0fe91ad9af9de35ffaf91dcdd41871b0a1bacb166391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea88c5abf5f30fca45d2a7daff6e7b1ddfd3003ca722d9c2f4b6e2bd87662896`

```dockerfile
```

-	Layers:
	-	`sha256:9402a4dc9677dff56f41041cd0c3ac6a481b0b58103190677fa95306f90dd1ac`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed27def1e4d1e40761b2b1578c8e2deaf73fc2b96f9e11f28c03f8b70713c993`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 16.7 KB (16677 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:11d819490d1e0c57b5b061274f9bc61ae318c0562d83efb62fd1015f1bf233ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272644038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bdd32af1842a4d2659f39093f8eccbc1f530f4f70d5fff6be544d0b9449b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:16:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6c2944a3e4a21302a0da032ef214c48cb9f90d1080bb8e7e5a91352da8a25f`  
		Last Modified: Tue, 18 Nov 2025 02:17:53 GMT  
		Size: 5.9 MB (5878013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d24a2d660d447f48321101946c660576d6cc6398982e88eabbe9c775f2694`  
		Last Modified: Tue, 18 Nov 2025 02:17:47 GMT  
		Size: 237.6 MB (237555950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecd266f7fb1d9e83c2f32cb3736bc25ec4774cc0e48c6dbb9e88eec8d96ad17`  
		Last Modified: Tue, 18 Nov 2025 02:17:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:55926a10717573cfefa42d136a7ac2bdfe777eeb02d64d07612991f429e74cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56248d7ceb4cfff8e6de0bde3aa70f0d0135762fa4e1327823e936b97c8fa40a`

```dockerfile
```

-	Layers:
	-	`sha256:2cd6b96b703977047157234643d1afdf22318a7c63e4d196ca867504d9518892`  
		Last Modified: Tue, 18 Nov 2025 06:04:44 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca04cfc1c6b84dff7aa8b2519d6c4a686e4596df58fe1d51abf1f65c92b2181`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 16.6 KB (16559 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:8d082d3a7e7a25545da61230d6fceaa10082c096d21937d1d7a4210121cd645d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b11a2f611440efabfebbd4c757f6df26c32ecbabd07c4c9720a14085623a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:15:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545cbd5cb3ec9f6e7b77c8c205f3530ef980328f28e70238a8f01a961d67006`  
		Last Modified: Tue, 18 Nov 2025 02:16:41 GMT  
		Size: 248.6 MB (248553764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c207300b970e725e6aa586c4daf1df0c17e96424840111b1042e770313f44f1`  
		Last Modified: Tue, 18 Nov 2025 02:16:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:592b7fe5984b3e4b42c2098f9dff3a1c81b5740a594d236f2f1d1b8b93c658d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f603dd87ba3035670e1ce7c406579dea1fdb731285bdaca11664a6de73f1bd46`

```dockerfile
```

-	Layers:
	-	`sha256:0f2987138af0e36f3f5dd87a6ec1be82c8215ee827989b8f809963942aeec870`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ce1020bfaaae1bf087a40ff5243eac648bcaf4ea4c6f325af3ccb2db2a942d`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 16.6 KB (16617 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-trixie`

```console
$ docker pull julia@sha256:4f1029237b1fb74831c13bbc626def18616e93ba0d47db0aa38ed71a2caf1333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11-trixie` - linux; amd64

```console
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 17:26:49 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Mon, 24 Nov 2025 04:21:22 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:6f9c2697e2a79bbb1ec77021b95238ed8a985a721748be7c4feb75cdb6424554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288855432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726b2c2f668e59b9ff7c1cc557ee81df169c5e608745b3b02e023c5e0d5cd538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:06:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 15:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:06:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb0ca605c9a4aa95330b7c16cb77d9773f3b80c4f94ee7019d057b54beaef0`  
		Last Modified: Tue, 18 Nov 2025 15:29:23 GMT  
		Size: 248.6 MB (248576032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf08d0a5c00f2c1f3ebd27f9cfa445162205a3c1e43d743b7a5610aec7c6742d`  
		Last Modified: Tue, 18 Nov 2025 15:08:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:592022e028c33e123281e031ca402bd1c920527d13752917b2a7d91a87bbd015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d469d9a4fd37934de0e7dacc608325aab02b88755e3e1750cd62aeb77968f7`

```dockerfile
```

-	Layers:
	-	`sha256:287af6c7630ed30d8e049560096bd452d5ca779fbb55a139181fce6f4b0d3aa1`  
		Last Modified: Tue, 18 Nov 2025 18:03:17 GMT  
		Size: 2.2 MB (2242674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69767a5e8bcd89c2bc3f71bceaced409601de9818a84d4716698fa787a816e0f`  
		Last Modified: Tue, 18 Nov 2025 18:03:19 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:f39ce3c0c4452cd4b8bb48d6c450406e1a97e489fbdcf604c45108b624a7223a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc92d61aa4d6379ee1a080d7ce3fc363fd49b454b56cc59922b525f5b2dedcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:8c85dee4e7029daaf9fe98159f6df607df9624343b01d932732b01fddc2290ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7`

```console
$ docker pull julia@sha256:7296f7aa7ceecef50a64b34d55a95cdbdd86c7bb6c4f6dc4388e56f0181862bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11.7` - linux; amd64

```console
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 17:26:49 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Mon, 24 Nov 2025 04:21:22 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; ppc64le

```console
$ docker pull julia@sha256:6f9c2697e2a79bbb1ec77021b95238ed8a985a721748be7c4feb75cdb6424554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288855432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726b2c2f668e59b9ff7c1cc557ee81df169c5e608745b3b02e023c5e0d5cd538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:06:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 15:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:06:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb0ca605c9a4aa95330b7c16cb77d9773f3b80c4f94ee7019d057b54beaef0`  
		Last Modified: Tue, 18 Nov 2025 15:29:23 GMT  
		Size: 248.6 MB (248576032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf08d0a5c00f2c1f3ebd27f9cfa445162205a3c1e43d743b7a5610aec7c6742d`  
		Last Modified: Tue, 18 Nov 2025 15:08:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:592022e028c33e123281e031ca402bd1c920527d13752917b2a7d91a87bbd015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d469d9a4fd37934de0e7dacc608325aab02b88755e3e1750cd62aeb77968f7`

```dockerfile
```

-	Layers:
	-	`sha256:287af6c7630ed30d8e049560096bd452d5ca779fbb55a139181fce6f4b0d3aa1`  
		Last Modified: Tue, 18 Nov 2025 18:03:17 GMT  
		Size: 2.2 MB (2242674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69767a5e8bcd89c2bc3f71bceaced409601de9818a84d4716698fa787a816e0f`  
		Last Modified: Tue, 18 Nov 2025 18:03:19 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-bookworm`

```console
$ docker pull julia@sha256:8b0ad8e6d29ed3767dcbc838f778c1f092fd68b9f7f4ff9060ee3fac461c9269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11.7-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:f4d3fac0fa62fb597cc498694fb26973346b837b9d14926dc8d5f6fc17d32c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c242212b04129672d2d70409ef0274ed477a2612e5db3c901967ea10d61ae11e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:21:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64287521fae1ed74e55d6db247c476f376f6326d8692b926ddaff00d264660e`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 5.7 MB (5716403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a695f03af55a8be1b1c5d34345a35e3f2d95d1ae0ce06fd24a16c32d0016110`  
		Last Modified: Tue, 18 Nov 2025 07:26:54 GMT  
		Size: 288.8 MB (288788343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4ab0dafaefcf335596cd20cdb877acd34f9746b8f0b69cc01f3f359b964eff`  
		Last Modified: Tue, 18 Nov 2025 04:22:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:93247f777bb0a6004b5af30109be1404066ebbce81229f9e8ccccb23ac61f450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc357a4f5c3b5ecb668442c6af292c7fa41801319ad9ba7489242ce108260aa8`

```dockerfile
```

-	Layers:
	-	`sha256:af0a12fa1bbaf70991bc885de8a505ad526520a0328a2ef2a64769262d6c565e`  
		Last Modified: Tue, 18 Nov 2025 06:04:34 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba641224ecb950287995cc172d09e26d07e19ad4ba0255e4ca5308125df15002`  
		Last Modified: Tue, 18 Nov 2025 06:04:35 GMT  
		Size: 16.6 KB (16583 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:919245c9db92ef7b659033cc127763743edc8ca281c0e225d0dcb2d9d8e89d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c9d30335a960582fb6e9f651d35c90d160ec47e42868e7f228fa83132cc743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18288eecc7d13e180b657797c35b3effcf06ed2ebd361ab629425ebc62a7bab8`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 5.6 MB (5567234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac828501f908b9f48f5885eadac374ee7f922484e46f80bc0c6ee521c97f0b0d`  
		Last Modified: Tue, 18 Nov 2025 15:58:28 GMT  
		Size: 304.6 MB (304646684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f5a7472d204b48f1950002bbd423e6cb2e6289962ce1c0f3c1df7c1006d92`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9c8015ebeb6a0e77e23f0fe91ad9af9de35ffaf91dcdd41871b0a1bacb166391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea88c5abf5f30fca45d2a7daff6e7b1ddfd3003ca722d9c2f4b6e2bd87662896`

```dockerfile
```

-	Layers:
	-	`sha256:9402a4dc9677dff56f41041cd0c3ac6a481b0b58103190677fa95306f90dd1ac`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed27def1e4d1e40761b2b1578c8e2deaf73fc2b96f9e11f28c03f8b70713c993`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 16.7 KB (16677 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:11d819490d1e0c57b5b061274f9bc61ae318c0562d83efb62fd1015f1bf233ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272644038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bdd32af1842a4d2659f39093f8eccbc1f530f4f70d5fff6be544d0b9449b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:16:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6c2944a3e4a21302a0da032ef214c48cb9f90d1080bb8e7e5a91352da8a25f`  
		Last Modified: Tue, 18 Nov 2025 02:17:53 GMT  
		Size: 5.9 MB (5878013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d24a2d660d447f48321101946c660576d6cc6398982e88eabbe9c775f2694`  
		Last Modified: Tue, 18 Nov 2025 02:17:47 GMT  
		Size: 237.6 MB (237555950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecd266f7fb1d9e83c2f32cb3736bc25ec4774cc0e48c6dbb9e88eec8d96ad17`  
		Last Modified: Tue, 18 Nov 2025 02:17:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:55926a10717573cfefa42d136a7ac2bdfe777eeb02d64d07612991f429e74cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56248d7ceb4cfff8e6de0bde3aa70f0d0135762fa4e1327823e936b97c8fa40a`

```dockerfile
```

-	Layers:
	-	`sha256:2cd6b96b703977047157234643d1afdf22318a7c63e4d196ca867504d9518892`  
		Last Modified: Tue, 18 Nov 2025 06:04:44 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca04cfc1c6b84dff7aa8b2519d6c4a686e4596df58fe1d51abf1f65c92b2181`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 16.6 KB (16559 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:8d082d3a7e7a25545da61230d6fceaa10082c096d21937d1d7a4210121cd645d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b11a2f611440efabfebbd4c757f6df26c32ecbabd07c4c9720a14085623a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:15:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545cbd5cb3ec9f6e7b77c8c205f3530ef980328f28e70238a8f01a961d67006`  
		Last Modified: Tue, 18 Nov 2025 02:16:41 GMT  
		Size: 248.6 MB (248553764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c207300b970e725e6aa586c4daf1df0c17e96424840111b1042e770313f44f1`  
		Last Modified: Tue, 18 Nov 2025 02:16:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:592b7fe5984b3e4b42c2098f9dff3a1c81b5740a594d236f2f1d1b8b93c658d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f603dd87ba3035670e1ce7c406579dea1fdb731285bdaca11664a6de73f1bd46`

```dockerfile
```

-	Layers:
	-	`sha256:0f2987138af0e36f3f5dd87a6ec1be82c8215ee827989b8f809963942aeec870`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ce1020bfaaae1bf087a40ff5243eac648bcaf4ea4c6f325af3ccb2db2a942d`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 16.6 KB (16617 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-trixie`

```console
$ docker pull julia@sha256:4f1029237b1fb74831c13bbc626def18616e93ba0d47db0aa38ed71a2caf1333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11.7-trixie` - linux; amd64

```console
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 17:26:49 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Mon, 24 Nov 2025 04:21:22 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:6f9c2697e2a79bbb1ec77021b95238ed8a985a721748be7c4feb75cdb6424554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288855432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726b2c2f668e59b9ff7c1cc557ee81df169c5e608745b3b02e023c5e0d5cd538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 15:06:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 15:06:46 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 15:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 15:06:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:06:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913a6b8fbfa7441b0703254c8da178ba3f6727d5cb336f9e314b7107edc15a5`  
		Last Modified: Tue, 18 Nov 2025 15:08:21 GMT  
		Size: 6.7 MB (6682172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb0ca605c9a4aa95330b7c16cb77d9773f3b80c4f94ee7019d057b54beaef0`  
		Last Modified: Tue, 18 Nov 2025 15:29:23 GMT  
		Size: 248.6 MB (248576032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf08d0a5c00f2c1f3ebd27f9cfa445162205a3c1e43d743b7a5610aec7c6742d`  
		Last Modified: Tue, 18 Nov 2025 15:08:20 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:592022e028c33e123281e031ca402bd1c920527d13752917b2a7d91a87bbd015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d469d9a4fd37934de0e7dacc608325aab02b88755e3e1750cd62aeb77968f7`

```dockerfile
```

-	Layers:
	-	`sha256:287af6c7630ed30d8e049560096bd452d5ca779fbb55a139181fce6f4b0d3aa1`  
		Last Modified: Tue, 18 Nov 2025 18:03:17 GMT  
		Size: 2.2 MB (2242674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69767a5e8bcd89c2bc3f71bceaced409601de9818a84d4716698fa787a816e0f`  
		Last Modified: Tue, 18 Nov 2025 18:03:19 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-windowsservercore`

```console
$ docker pull julia@sha256:f39ce3c0c4452cd4b8bb48d6c450406e1a97e489fbdcf604c45108b624a7223a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11.7-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc92d61aa4d6379ee1a080d7ce3fc363fd49b454b56cc59922b525f5b2dedcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:8c85dee4e7029daaf9fe98159f6df607df9624343b01d932732b01fddc2290ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.11.7-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12`

```console
$ docker pull julia@sha256:854de5495d7a932103bb164923ea40441ee2f7e2c95f2eb7edac6a0f81eeb1e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-bookworm`

```console
$ docker pull julia@sha256:0feea4981d0f0b0ef007df377a3afac39c6fbcdc0b509330c789376a60a8b3a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:ebd943bccbcb194f9d5f0bb771d1064f124995ede9bc90baf866d62a06ac0cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323892306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea21809e86116583b0d88dfa11d5f5b9b4204351012c09219670025116e98d0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:38:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede5ccf9c6259cfc06511259b60c6ac73ba7f2fe6a4fc52f629ead8f70a1137b`  
		Last Modified: Mon, 24 Nov 2025 22:39:58 GMT  
		Size: 5.7 MB (5716408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f681efbbc76aebdf3eea9d90ede7a11f9d56bf62c6604abaacfe8f572ef1dc`  
		Last Modified: Tue, 25 Nov 2025 00:17:15 GMT  
		Size: 289.9 MB (289947080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20c522aa2e3a84dd11ed978edfd648fd25db01e32b9239f9534d62c1b5b6e6b`  
		Last Modified: Mon, 24 Nov 2025 22:39:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3ef845e7f11dc238ebe4eb7f322e328fda60575f7646774abbccff44f1360da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd24da63876208897d7ff6207bd15c671cedbdd26e453242baf5db8046deef90`

```dockerfile
```

-	Layers:
	-	`sha256:0ebb24515878f7357c14bdbff5a2548fbb94661e40603ca0ffb4e02c111a194a`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc92f28800b448530c7176f4f615cb2258c03bf1e94bbeb1731e00658a1ef67c`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3dfc6b09e66f688b9901969cab733eadaa7e456bcad3c4cecee5e297e6072fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344622258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9e2abe7468fc884efc51e7726c46898d3f2e934faa2f5d11f661cf4700a94a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:39:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560374fb6f10760919cfedfebbba3b0f6ec46de28729df786cba4c8fc3fdd7bb`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 5.6 MB (5567216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850889d615ff2706ab9dcd96187e71512e172e8717102b5c174265725c2098b7`  
		Last Modified: Tue, 25 Nov 2025 00:17:47 GMT  
		Size: 311.0 MB (310952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e26358d6614ef2e86eb4e97171e43030aa04c143e5d26e34d63c20b4873d42`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:abfa0f12c098fa7adff539a01c0ccfa25a52b1ca703b39eaac97ccd872d3b72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88acdcedeb7569b9be9bf9022215da5e51daef9e7fe15a146ad685467cb07923`

```dockerfile
```

-	Layers:
	-	`sha256:8fb1bdaf1f81e85bb42847721687590cccea14a6a68f2f31636b44bbff262e87`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ad70d36ab4a56fa2a3bc6d3bc715247173fdf1f572003787265991ef8de6a3`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; 386

```console
$ docker pull julia@sha256:f755775da5f3613be0b4655c9d19a72c4208776e2af4dafe26f51ea85a639f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266222757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a22b792e310d5f7def5af8d56e49eaa65335bd523a826b14c2394ff0d581f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd7b893f16d80738b2e0d480c2c48dcc9a045a3df6d084caf564d380eba3588`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 5.9 MB (5877997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b706a608f58d09d21fca9473fa23c5a70796cfd9eab3f397ab722205461fa6a`  
		Last Modified: Tue, 25 Nov 2025 00:16:56 GMT  
		Size: 231.1 MB (231134686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f76d01befd1d4895eb64055e752e8d64d28b21b10ef46110f60b17c84a7290`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3801140c193396ba8c6c7c3d7dec41496528dce0744a1a511936c7bfe3ec341f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cc08585cd4984bc999ff1276105e3c4c35776821144b00e3f2401d932cb206`

```dockerfile
```

-	Layers:
	-	`sha256:851a3ee9b0a8eaf1dc0fc439a91f4a546435d070254ba43d269e7f86405cd9be`  
		Last Modified: Tue, 25 Nov 2025 00:02:46 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b279851a6615b5c52a4c4c6da944b3681413b200a24becb1add45bd2d3bdad4`  
		Last Modified: Tue, 25 Nov 2025 00:02:47 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-trixie`

```console
$ docker pull julia@sha256:d3dc1f6f39a492829c6e74eaa2a26f68d3dcba577b1ddae9960f83ad4626d9b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12-trixie` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-windowsservercore`

```console
$ docker pull julia@sha256:11aee8627b47e4ed5e908a587ae55c98c86ccd8117f65566a96f1ee0ddf742b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:543d2532e513d8a1a42648f9dc78c42b9ce1a8a2d68676b185fbd36c75ec2dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:ec852fdf68ade5279f9b5ef65a1833e073d343f9bc224b63bf1caabcd4a9e38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.12-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.2`

```console
$ docker pull julia@sha256:854de5495d7a932103bb164923ea40441ee2f7e2c95f2eb7edac6a0f81eeb1e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12.2` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.2` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.2` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.2` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.2` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.2-bookworm`

```console
$ docker pull julia@sha256:0feea4981d0f0b0ef007df377a3afac39c6fbcdc0b509330c789376a60a8b3a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.2-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:ebd943bccbcb194f9d5f0bb771d1064f124995ede9bc90baf866d62a06ac0cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323892306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea21809e86116583b0d88dfa11d5f5b9b4204351012c09219670025116e98d0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:38:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede5ccf9c6259cfc06511259b60c6ac73ba7f2fe6a4fc52f629ead8f70a1137b`  
		Last Modified: Mon, 24 Nov 2025 22:39:58 GMT  
		Size: 5.7 MB (5716408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f681efbbc76aebdf3eea9d90ede7a11f9d56bf62c6604abaacfe8f572ef1dc`  
		Last Modified: Tue, 25 Nov 2025 00:17:15 GMT  
		Size: 289.9 MB (289947080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20c522aa2e3a84dd11ed978edfd648fd25db01e32b9239f9534d62c1b5b6e6b`  
		Last Modified: Mon, 24 Nov 2025 22:39:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3ef845e7f11dc238ebe4eb7f322e328fda60575f7646774abbccff44f1360da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd24da63876208897d7ff6207bd15c671cedbdd26e453242baf5db8046deef90`

```dockerfile
```

-	Layers:
	-	`sha256:0ebb24515878f7357c14bdbff5a2548fbb94661e40603ca0ffb4e02c111a194a`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc92f28800b448530c7176f4f615cb2258c03bf1e94bbeb1731e00658a1ef67c`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3dfc6b09e66f688b9901969cab733eadaa7e456bcad3c4cecee5e297e6072fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344622258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9e2abe7468fc884efc51e7726c46898d3f2e934faa2f5d11f661cf4700a94a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:39:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560374fb6f10760919cfedfebbba3b0f6ec46de28729df786cba4c8fc3fdd7bb`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 5.6 MB (5567216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850889d615ff2706ab9dcd96187e71512e172e8717102b5c174265725c2098b7`  
		Last Modified: Tue, 25 Nov 2025 00:17:47 GMT  
		Size: 311.0 MB (310952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e26358d6614ef2e86eb4e97171e43030aa04c143e5d26e34d63c20b4873d42`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:abfa0f12c098fa7adff539a01c0ccfa25a52b1ca703b39eaac97ccd872d3b72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88acdcedeb7569b9be9bf9022215da5e51daef9e7fe15a146ad685467cb07923`

```dockerfile
```

-	Layers:
	-	`sha256:8fb1bdaf1f81e85bb42847721687590cccea14a6a68f2f31636b44bbff262e87`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ad70d36ab4a56fa2a3bc6d3bc715247173fdf1f572003787265991ef8de6a3`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.2-bookworm` - linux; 386

```console
$ docker pull julia@sha256:f755775da5f3613be0b4655c9d19a72c4208776e2af4dafe26f51ea85a639f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266222757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a22b792e310d5f7def5af8d56e49eaa65335bd523a826b14c2394ff0d581f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd7b893f16d80738b2e0d480c2c48dcc9a045a3df6d084caf564d380eba3588`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 5.9 MB (5877997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b706a608f58d09d21fca9473fa23c5a70796cfd9eab3f397ab722205461fa6a`  
		Last Modified: Tue, 25 Nov 2025 00:16:56 GMT  
		Size: 231.1 MB (231134686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f76d01befd1d4895eb64055e752e8d64d28b21b10ef46110f60b17c84a7290`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3801140c193396ba8c6c7c3d7dec41496528dce0744a1a511936c7bfe3ec341f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cc08585cd4984bc999ff1276105e3c4c35776821144b00e3f2401d932cb206`

```dockerfile
```

-	Layers:
	-	`sha256:851a3ee9b0a8eaf1dc0fc439a91f4a546435d070254ba43d269e7f86405cd9be`  
		Last Modified: Tue, 25 Nov 2025 00:02:46 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b279851a6615b5c52a4c4c6da944b3681413b200a24becb1add45bd2d3bdad4`  
		Last Modified: Tue, 25 Nov 2025 00:02:47 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.2-trixie`

```console
$ docker pull julia@sha256:d3dc1f6f39a492829c6e74eaa2a26f68d3dcba577b1ddae9960f83ad4626d9b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.2-trixie` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.2-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.2-trixie` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.2-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.2-windowsservercore`

```console
$ docker pull julia@sha256:11aee8627b47e4ed5e908a587ae55c98c86ccd8117f65566a96f1ee0ddf742b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12.2-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.2-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.2-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:543d2532e513d8a1a42648f9dc78c42b9ce1a8a2d68676b185fbd36c75ec2dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.2-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:ec852fdf68ade5279f9b5ef65a1833e073d343f9bc224b63bf1caabcd4a9e38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.12.2-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:0feea4981d0f0b0ef007df377a3afac39c6fbcdc0b509330c789376a60a8b3a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:ebd943bccbcb194f9d5f0bb771d1064f124995ede9bc90baf866d62a06ac0cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323892306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea21809e86116583b0d88dfa11d5f5b9b4204351012c09219670025116e98d0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:38:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede5ccf9c6259cfc06511259b60c6ac73ba7f2fe6a4fc52f629ead8f70a1137b`  
		Last Modified: Mon, 24 Nov 2025 22:39:58 GMT  
		Size: 5.7 MB (5716408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f681efbbc76aebdf3eea9d90ede7a11f9d56bf62c6604abaacfe8f572ef1dc`  
		Last Modified: Tue, 25 Nov 2025 00:17:15 GMT  
		Size: 289.9 MB (289947080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20c522aa2e3a84dd11ed978edfd648fd25db01e32b9239f9534d62c1b5b6e6b`  
		Last Modified: Mon, 24 Nov 2025 22:39:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3ef845e7f11dc238ebe4eb7f322e328fda60575f7646774abbccff44f1360da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd24da63876208897d7ff6207bd15c671cedbdd26e453242baf5db8046deef90`

```dockerfile
```

-	Layers:
	-	`sha256:0ebb24515878f7357c14bdbff5a2548fbb94661e40603ca0ffb4e02c111a194a`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc92f28800b448530c7176f4f615cb2258c03bf1e94bbeb1731e00658a1ef67c`  
		Last Modified: Tue, 25 Nov 2025 00:02:37 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3dfc6b09e66f688b9901969cab733eadaa7e456bcad3c4cecee5e297e6072fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344622258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9e2abe7468fc884efc51e7726c46898d3f2e934faa2f5d11f661cf4700a94a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:39:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:27 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560374fb6f10760919cfedfebbba3b0f6ec46de28729df786cba4c8fc3fdd7bb`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 5.6 MB (5567216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850889d615ff2706ab9dcd96187e71512e172e8717102b5c174265725c2098b7`  
		Last Modified: Tue, 25 Nov 2025 00:17:47 GMT  
		Size: 311.0 MB (310952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e26358d6614ef2e86eb4e97171e43030aa04c143e5d26e34d63c20b4873d42`  
		Last Modified: Mon, 24 Nov 2025 22:40:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:abfa0f12c098fa7adff539a01c0ccfa25a52b1ca703b39eaac97ccd872d3b72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88acdcedeb7569b9be9bf9022215da5e51daef9e7fe15a146ad685467cb07923`

```dockerfile
```

-	Layers:
	-	`sha256:8fb1bdaf1f81e85bb42847721687590cccea14a6a68f2f31636b44bbff262e87`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ad70d36ab4a56fa2a3bc6d3bc715247173fdf1f572003787265991ef8de6a3`  
		Last Modified: Tue, 25 Nov 2025 00:02:42 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:f755775da5f3613be0b4655c9d19a72c4208776e2af4dafe26f51ea85a639f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266222757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a22b792e310d5f7def5af8d56e49eaa65335bd523a826b14c2394ff0d581f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Mon, 24 Nov 2025 22:40:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:03 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd7b893f16d80738b2e0d480c2c48dcc9a045a3df6d084caf564d380eba3588`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 5.9 MB (5877997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b706a608f58d09d21fca9473fa23c5a70796cfd9eab3f397ab722205461fa6a`  
		Last Modified: Tue, 25 Nov 2025 00:16:56 GMT  
		Size: 231.1 MB (231134686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f76d01befd1d4895eb64055e752e8d64d28b21b10ef46110f60b17c84a7290`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3801140c193396ba8c6c7c3d7dec41496528dce0744a1a511936c7bfe3ec341f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cc08585cd4984bc999ff1276105e3c4c35776821144b00e3f2401d932cb206`

```dockerfile
```

-	Layers:
	-	`sha256:851a3ee9b0a8eaf1dc0fc439a91f4a546435d070254ba43d269e7f86405cd9be`  
		Last Modified: Tue, 25 Nov 2025 00:02:46 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b279851a6615b5c52a4c4c6da944b3681413b200a24becb1add45bd2d3bdad4`  
		Last Modified: Tue, 25 Nov 2025 00:02:47 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:854de5495d7a932103bb164923ea40441ee2f7e2c95f2eb7edac6a0f81eeb1e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:trixie`

```console
$ docker pull julia@sha256:d3dc1f6f39a492829c6e74eaa2a26f68d3dcba577b1ddae9960f83ad4626d9b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:trixie` - linux; amd64

```console
$ docker pull julia@sha256:79ca4f8b7bce61c2e71828d2a9f57b1f1d22c32b15685d43aa894fbad931a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ab0e34e23fd2fd5e2c3a5ef8bb32583807e0dc57a95df9a1dc4bfc1f1bb436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:35 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc5a17d3477057561d76149e6cab1681352f0d1831883dacea1a7276eee7a7`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 6.2 MB (6242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985a335632124fa3146b68d609bda9dd931e48a7a488822c9d09e0f2e0282670`  
		Last Modified: Mon, 24 Nov 2025 23:29:29 GMT  
		Size: 290.0 MB (289981908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9c319adf4228067a1aa81c1bf1f1f5a4550d911d6687e26dff484bc2a640d`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6a633922233eefe8a3df53bd9d8433968f17312bf60e7f432fcb0a882d2cc617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4559e6795114a79b04dd6e46d161f5a34247dab26d96b5b71ae660b72630987`

```dockerfile
```

-	Layers:
	-	`sha256:475445ac7f17c199b05865cfce9c04d6a1fb4b7791d53cabc00e8e17be420ab3`  
		Last Modified: Tue, 25 Nov 2025 00:02:27 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2368c86d4f09d7300b83704a8042d2409e8b38569db007873ac6fa6ad87cf7`  
		Last Modified: Tue, 25 Nov 2025 00:02:28 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd00828b2e5a2b6a669d526de9cf34343a71ac47902e49866a63f2e57f08f6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067a679311bd33e93d0c0f8c4e5f050bd58c6f9f68025b827ab27a43348f2d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:39:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:39:20 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:39:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:39:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ad3172ab2c33b0d84bd69d598dda71ba12a5948af1f7b5095300fcf7322bc`  
		Last Modified: Mon, 24 Nov 2025 22:40:19 GMT  
		Size: 6.2 MB (6153476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f43bd96dfacec48547a2e2171b9774eed357bbb99e2abc7c1153f895cf81e`  
		Last Modified: Mon, 24 Nov 2025 23:12:54 GMT  
		Size: 311.0 MB (310983831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dc27dd1e8abc4163dfb4397f7aff1157c2b2e5ebc00b6b4c4c5cc29ce4a600`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:43c3af6f66c0c884132905b803d01a1eb55733fd95d3a2b185b8994995b98f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd6b0a4b4c2505435af412069dd0ff3ce2451da96d40f5419714b7e644bb8b`

```dockerfile
```

-	Layers:
	-	`sha256:388adfc977249b2345efd6989ddf16b84558ebe2fbb6c0948852a64e6b7ebfeb`  
		Last Modified: Tue, 25 Nov 2025 00:02:33 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7eb7d5ee252725e1d3ad9eea80321bcc524f74ed6576ec2c98ed0309507bc`  
		Last Modified: Tue, 25 Nov 2025 00:02:34 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:2b4911770d55f2ce1cfaa9e65212e935b293b3072a24c78e86d958400021b7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6226064be8f684a4aa38485341f328beb79acf659dddd57403d21e3afd2da546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Mon, 24 Nov 2025 22:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 24 Nov 2025 22:41:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 24 Nov 2025 22:41:02 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:41:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 22:41:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfea3c551bdfc8fea542dc2d195e2484afcb7dce6a487fc0aacbe7e2972fe9f`  
		Last Modified: Mon, 24 Nov 2025 22:41:50 GMT  
		Size: 6.4 MB (6427688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38b8d981a68f4abbeca9ed617e2cc6b41a8454d53304283e7634156de646cd`  
		Last Modified: Mon, 24 Nov 2025 22:49:40 GMT  
		Size: 231.2 MB (231168772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a9afa9664d75fce73172618bee5c3c7af2eaa80aa2925878d7859e2036a6b`  
		Last Modified: Mon, 24 Nov 2025 22:41:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5806cd246dfd087a3a88db228417aa0ebad8cca31277a06fa8a100d857452ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9430b7952cb3cdbc161c2d74d2f6bb40ddb4c70f4cae39fa23c3f0a749f039d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e38654f35d7675e6ba31cc81a59c33bdc6623f0e52d828f73b8f7dcfff9c71`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d8ddf0d5fdadad4d0ab0eb4e1ab8906978d43cd7dc3fb5d139a2f493a76030`  
		Last Modified: Tue, 25 Nov 2025 00:02:38 GMT  
		Size: 17.6 KB (17629 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:11aee8627b47e4ed5e908a587ae55c98c86ccd8117f65566a96f1ee0ddf742b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:543d2532e513d8a1a42648f9dc78c42b9ce1a8a2d68676b185fbd36c75ec2dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:b19a0355653e5bcf77bd963149b5b0d5daee9d33495c665554f25360d61575fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156065454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff53739fcaa993184fc9260a3e1520a8d2b789ada88a284fc7383f281ff09cb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Mon, 24 Nov 2025 21:54:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:35:00 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:39:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:39:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aad132d44253f5455efa330566900fe031331917e6f95f4055d2072ead42290`  
		Last Modified: Mon, 24 Nov 2025 22:10:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b500a462b83a39b4fcad48acc61a24d9e5de87a8720e03bdf25e13feb4ba`  
		Last Modified: Mon, 24 Nov 2025 22:40:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b738f0f264c3ca50e1f4bb1b056a9c9b262ce66bc0b3c7f5a9ac92ee37cb5`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc7adf8835efbc83d4960db10242b44009e37c8653b8b5081d79d18e21bfcfa`  
		Last Modified: Mon, 24 Nov 2025 22:40:33 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3eb5dffd1df8b0325f75b73663fb4dcfe07865e4523235c38b62f88a0389f`  
		Last Modified: Tue, 25 Nov 2025 00:03:05 GMT  
		Size: 386.1 MB (386097304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d1c145a6db855fb1b3f59e92beac660753ab469d40ddf7e32f5efe7907521`  
		Last Modified: Mon, 24 Nov 2025 22:40:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:ec852fdf68ade5279f9b5ef65a1833e073d343f9bc224b63bf1caabcd4a9e38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:1990bf7cea84ad93676904e2ebcc962fb7a4e6f6237e64f41e853e8d5049af2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3621480357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb7ffaa2038efb8c28b39df07c12d7507e55638540c1cb2c254f6b158bc054`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Mon, 24 Nov 2025 21:55:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Nov 2025 22:34:55 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Mon, 24 Nov 2025 22:34:56 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Mon, 24 Nov 2025 22:36:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 24 Nov 2025 22:36:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbc05ed4b88c9841b3c2e452d7b00e7b0a7c04e26a7cb1757ba50deeefc6513`  
		Last Modified: Mon, 24 Nov 2025 22:17:06 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab0704401bd269c0af9a60de35b69b7145b145dff03d99162674963b1ae9e8`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f95755a28521a2ff15fedf6363ad611cd23f19479f5fe3e8a2d4a2c7c73028d`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c7e6a745ebdda612b1ae9cc1eb18926529eccfb07b6c96ef5c91fef454cf7`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041ece9d80558f66d11f53fb09bfb6b522931d7620ad75b3f9110af908ccc1c`  
		Last Modified: Tue, 25 Nov 2025 00:03:18 GMT  
		Size: 386.0 MB (386018008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23c9e1a5b20064db589fe95898251bdb204cdfe84adebb7a683bfa6fc07adfd`  
		Last Modified: Mon, 24 Nov 2025 22:38:03 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
