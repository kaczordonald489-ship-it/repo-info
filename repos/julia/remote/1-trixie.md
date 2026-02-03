## `julia:1-trixie`

```console
$ docker pull julia@sha256:4cd83152cc19cc8c747abf8e3844ef23c75f7d8d8dc654cb725eff8cd69c7a74
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
$ docker pull julia@sha256:e9a759bc6cc5ef6f5557f04c0e44c397124772108e4a5930e9e4bb4e80555ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325878060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0c0f5ea8cff1980a8826c6bb6f5691ca428e01f773bd8938cc61595b728d18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Feb 2026 02:21:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:21:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Feb 2026 02:21:41 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 03 Feb 2026 02:21:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Feb 2026 02:21:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:21:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:21:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3e99e7ce42482d6f421b6c05e1343768c1e000859146860e53a7e4390f6ead`  
		Last Modified: Tue, 03 Feb 2026 02:22:24 GMT  
		Size: 6.2 MB (6243655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f7351381c8d1cb1ad78e764644a7bda35392e9d646fadacf1e024cb32e9acf`  
		Last Modified: Tue, 03 Feb 2026 02:22:30 GMT  
		Size: 289.9 MB (289855437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e8670cbf70027762de7c39840761e7d0826de92ca4126f403ba9c87eef2fbf`  
		Last Modified: Tue, 03 Feb 2026 02:22:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f992b5a6c62421b0ae3ddb5ba0c706f7d4887f13e4ba2b46aeeedd787290ea00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95083aef1fab984b141fce56c07dbf057ebd0630c819bd5669b09baab9d8313`

```dockerfile
```

-	Layers:
	-	`sha256:7c5ad1bbfe4d7d9369794dcc0a3842e094f3da8a2d54edebc6bb31aec37a0bdc`  
		Last Modified: Tue, 03 Feb 2026 02:22:24 GMT  
		Size: 2.2 MB (2240221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46fd5adc320496b1aa8e3fb04eac17db0b4a8f7b8c2855513909762d766b4f1`  
		Last Modified: Tue, 03 Feb 2026 02:22:23 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1339c3a525d63f7089e9d51aa7dce030d432a2b9111cb2350cb6a6202f796ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.6 MB (347589109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de34128b1e04e457ee87ce7e6e12d26f737ad26d09a978fedfcd1b25f3f16dab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:20:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:21:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Feb 2026 02:21:23 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 03 Feb 2026 02:21:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Feb 2026 02:21:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:21:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da8f60a6878eb274b54d3b42dc4e42457a7420be8806cb3d1c6aeded584eafc`  
		Last Modified: Tue, 03 Feb 2026 02:22:07 GMT  
		Size: 6.2 MB (6150927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdb6e84da911fbd1d7eb19c7ea19c6170d71c9cd24de103e5dbd9b3126de7f`  
		Last Modified: Tue, 03 Feb 2026 02:22:13 GMT  
		Size: 311.3 MB (311297749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6abb2aa6dde0a09353db3bec7ffcc67ba9063c037046fbd79fb5fec2bd8b7e`  
		Last Modified: Tue, 03 Feb 2026 02:22:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6d0d7cdc2159a3404ae7b157f4421ea042d486cdf119b52e7b4eda5187138400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4949e52dfa912e6e0fd5fed11cfef86e45de26172a0c3f956882609a2c48a7`

```dockerfile
```

-	Layers:
	-	`sha256:b794027d7d740621e4974b7000b6f0c5eceec34cbbb22259707f067dd9d94576`  
		Last Modified: Tue, 03 Feb 2026 02:22:07 GMT  
		Size: 2.2 MB (2240553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef00d5af53f9464327d53addc715b45dcf3291643b51880306a2125288f075f1`  
		Last Modified: Tue, 03 Feb 2026 02:22:07 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:9cfba673303bff3628f3cbef5bb2e3fd4de114079c23e8f5ce2d5e3fbb755c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268970183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ac9525aaa7a63bd5d85d23a8599300bbcdeb5f3a3b6951865523628568dc44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Feb 2026 02:17:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:17:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Feb 2026 02:17:51 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 03 Feb 2026 02:17:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Feb 2026 02:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:17:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb8d4d1efd1f2cc74db06ac3995a5e1c97d9d8c2aec1e7cf4289c7465cb8817`  
		Last Modified: Tue, 03 Feb 2026 02:18:22 GMT  
		Size: 6.4 MB (6429457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c20649f58ef6c626d005424892558597ec1b59b15c566add9a80ff9a2f285b`  
		Last Modified: Tue, 03 Feb 2026 02:18:26 GMT  
		Size: 231.2 MB (231246497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd2a23d3eb74c312136f125360a8e6a91c67acf7bc39d053a972da2fc13ed84`  
		Last Modified: Tue, 03 Feb 2026 02:18:22 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2aeed5af55c2fa816a5dfd517e862b4e6880bb5458bb146f4686ca7814ffcffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db06d508d9c3326c61e263e51af712fe389e306fb17a646f2992dd483f2f262a`

```dockerfile
```

-	Layers:
	-	`sha256:dc5208a3959cf8a0edd7f6e90d2cbf901131a222f691e699fab09804ebfc6945`  
		Last Modified: Tue, 03 Feb 2026 02:18:22 GMT  
		Size: 2.2 MB (2237346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541e6e7ba062a25319fba5014518fe38e24b36ced428124330615c475b587317`  
		Last Modified: Tue, 03 Feb 2026 02:18:22 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json
