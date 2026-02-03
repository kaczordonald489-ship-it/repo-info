## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:d447ab8733d39c05328f5b8382db9a8d7da35349a173c320e5682547a15d1118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:578267d5313490b1717283aa140bfe6277c033a5c718c4cf9fd2267cc923c526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342482201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d107c72e83bb90bb8734fa2fb038d68908c7741e06060f8b09f0df03a794ec03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:22:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:22:52 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Feb 2026 02:22:52 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:52 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Feb 2026 02:22:52 GMT
ENV JULIA_VERSION=1.13.0-beta1
# Tue, 03 Feb 2026 02:22:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta1-linux-x86_64.tar.gz'; 			sha256='4b501de5f7bdff4fd4ab186e2fae8608ea4cf840c6bbcee142362a1a32a0f354'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta1-linux-i686.tar.gz'; 			sha256='7875f846c550f332988ee7466a120e0ff1040b05d54d4889db496ef7cae5d131'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta1-linux-aarch64.tar.gz'; 			sha256='73624a83a7ac1effcfeaeaf9cd9668113b6ef3b3d6135f9e9259a8b83a9fd75d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Feb 2026 02:22:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:22:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9469bd98bfaae26c69ba234a49453c30f5c6a3aa4631503d68f738f213a38bcb`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 5.7 MB (5718045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1deb120071ab55bdc77770fd27ed4b6052ecc3d8c4ce17912493dcfc70a9b7`  
		Last Modified: Tue, 03 Feb 2026 02:23:46 GMT  
		Size: 308.5 MB (308535299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9fd8fd26160cda63bd9435f09081faf35af27eea6fb818b0f1c36e9849e5e4`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:cf00a4456f885f68f05300a47b3490de16081bb93047564657b30019c6790803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f474890d6131c5a39904ec01b0f7a3ed9770b05aae14bdfa59e93c8a6599739`

```dockerfile
```

-	Layers:
	-	`sha256:e4162a8a4706c1cf3104d318dc9b236646a96e1432cdfb364d2c3d11f74d70cf`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 2.6 MB (2568624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aec3abc3b6454152cd35c155a9a868789f32299db6263559f57b729ef70e62b`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 16.3 KB (16319 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5d1c444528c675aebc7d00a8ed173549dacd4b6ccf61622cd72c9111698e068a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366094372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e580bc141168c98afd4f72fa68ad93885e59891e5569a3ee264810288d89a671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:22:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:22:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Feb 2026 02:22:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Feb 2026 02:22:50 GMT
ENV JULIA_VERSION=1.13.0-beta1
# Tue, 03 Feb 2026 02:22:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta1-linux-x86_64.tar.gz'; 			sha256='4b501de5f7bdff4fd4ab186e2fae8608ea4cf840c6bbcee142362a1a32a0f354'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta1-linux-i686.tar.gz'; 			sha256='7875f846c550f332988ee7466a120e0ff1040b05d54d4889db496ef7cae5d131'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta1-linux-aarch64.tar.gz'; 			sha256='73624a83a7ac1effcfeaeaf9cd9668113b6ef3b3d6135f9e9259a8b83a9fd75d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Feb 2026 02:22:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:22:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:22:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01beea876d94aa153db5579554d8ae8331f39707b7dbce62efd40ea51cc2888d`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 5.6 MB (5567890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ca360d219f3a239a1af4cbfca00e995528b1141d6978951c14f8ecf57eca13`  
		Last Modified: Tue, 03 Feb 2026 02:23:45 GMT  
		Size: 332.4 MB (332418287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21afba0dafb9031a824ef70422de34ed020dbae4decef6a6f274d0c48a9a6872`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:fedfe8f0850dfb7cb8b2305c3adc3520ce1618ffc361338063d0e4c11db45dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7fb3b6199a8fe95a2b0fc5e9c2643180ab0a70c9c481fae690e0165eec4bcd`

```dockerfile
```

-	Layers:
	-	`sha256:ad498b7f4a7419df38e912cc1f77fa914899093a5ac47a09a1f0aba326a7e962`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 2.6 MB (2568887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47db780ab2ca39da96b7474635277438f8f135a5e6511129422606856ad9891f`  
		Last Modified: Tue, 03 Feb 2026 02:23:39 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:262716831493d04b17c0e04b0c6771a8552b1a0b5c586dd83cec11de67958081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278022183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8c5676d167fc8df5304d65d24aa4b44c24dea0b97ec89a9220648bbefd201c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 03 Feb 2026 02:18:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:18:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 03 Feb 2026 02:18:30 GMT
ENV JULIA_VERSION=1.13.0-beta1
# Tue, 03 Feb 2026 02:18:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta1-linux-x86_64.tar.gz'; 			sha256='4b501de5f7bdff4fd4ab186e2fae8608ea4cf840c6bbcee142362a1a32a0f354'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta1-linux-i686.tar.gz'; 			sha256='7875f846c550f332988ee7466a120e0ff1040b05d54d4889db496ef7cae5d131'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta1-linux-aarch64.tar.gz'; 			sha256='73624a83a7ac1effcfeaeaf9cd9668113b6ef3b3d6135f9e9259a8b83a9fd75d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 03 Feb 2026 02:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c185bdb4d4f995d7cd102f7a448db41ca799a3cdbc830d48938b000c145be9`  
		Last Modified: Tue, 03 Feb 2026 02:19:06 GMT  
		Size: 5.9 MB (5878863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d412bab4c9f40290bab2dcac60b33fb3c2a5e7e222a2c46c9a1daffc310c1e`  
		Last Modified: Tue, 03 Feb 2026 02:19:11 GMT  
		Size: 242.9 MB (242932933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed33d3d55db624e4d7f0fc2bd0ce04e7d96492143e669a7338dfdf20cc3aad`  
		Last Modified: Tue, 03 Feb 2026 02:19:06 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:dd62405574574e41de486e3e43c96cf3fe9899b2a78185d0bd28faadc49bc108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabbcd8a71c4991714c3a58ec04786bef9787c765400551932f75039e2ab85f6`

```dockerfile
```

-	Layers:
	-	`sha256:90630fbbbd9f90c9e1b4945ac4d825f5cf0553169c9fbab920410ebab657e7b6`  
		Last Modified: Tue, 03 Feb 2026 02:19:06 GMT  
		Size: 2.6 MB (2565776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8936795c333b94cf9301a39c50a6fa0af575c7f17e675710eb09aef0881a7b8`  
		Last Modified: Tue, 03 Feb 2026 02:19:05 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
