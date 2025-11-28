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
