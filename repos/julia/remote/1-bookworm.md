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
