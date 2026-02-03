## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:c6bbe9f5afdde1be5e15a9973e1ac27300c175e2d1e5bf538304b097a8076c0c
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:e2dbb426611be51b4098d0a8102bc150db4949af579ceb2e0a0eda4ffea6a879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322682930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e1c9c23a0c956be9dbf935dac4fd7e865cd7b15a09615bdcbf1ad63572b958`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:16:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:16:53 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:16:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:16:53 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:19:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:19:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd254524f0e16da3c13c41ee383e6d5e22a91f535cf36d4bd045b1ccd346a477`  
		Last Modified: Tue, 03 Feb 2026 05:20:06 GMT  
		Size: 92.4 MB (92433463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca55bbd490d4f215c5420355c680b71279036da5d7c91d2d678e32c231a9c9`  
		Last Modified: Mon, 02 Feb 2026 19:30:41 GMT  
		Size: 93.3 MB (93333409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a7969ad3fcac25a52bbdc7ae049c248fe06ff3158c8aa02155f1a1a82ad54f`  
		Last Modified: Tue, 03 Feb 2026 05:20:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b23e0de44e9c814a687ab7b2f997013bce0e33756228c5b0fd490d0ae71d77f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b95ea672f324250412de578d05a48d43f31666ffe999048c2b51160a6efaff4`

```dockerfile
```

-	Layers:
	-	`sha256:f44ae9f5758d62bc190f617ead4eeb8d754d69dcc4b5f8ec4d432715f8e933d2`  
		Last Modified: Tue, 03 Feb 2026 05:20:04 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dde2fb271cb069b59dec12a477e4252247503ebb0e9ae7d48c22da176bd2030`  
		Last Modified: Tue, 03 Feb 2026 05:20:04 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:792e1418f4a60e2b967c0d16f792da17732bf068161535dbbcec4b360d2cf10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281558278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c79d2cbe05814a4b1dc1c4a9f6d9f91ecbb3e58f59846869cab876842f65fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:18:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:21:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 06:21:33 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 06:21:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 06:21:33 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 06:21:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 06:21:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215004933fb3174b490417af4009cc5994b534b00700ca696692f3d7aae5a99`  
		Last Modified: Tue, 03 Feb 2026 06:22:00 GMT  
		Size: 66.3 MB (66288951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c4d8d165092e2ffa5f6928ecd151df0b8f3dc1362c8f59dcd6d9b09df5017`  
		Last Modified: Mon, 02 Feb 2026 19:30:25 GMT  
		Size: 89.5 MB (89476429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d016ee69557538f963192a15d268af1a3d9c8b897cc9b9f9ef226013e491ee9`  
		Last Modified: Tue, 03 Feb 2026 06:21:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b35652a8c7810e184b9e5e0b411f11029aae82c5e682aa335733160b918fe9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd442577f4566ba8e4010ca1a6b6c2f2795b2dde763621c62632af48d49eccf`

```dockerfile
```

-	Layers:
	-	`sha256:65df49920a778fea851a6f57a5240ed763c449c5a213a7d0329c5e9359a15596`  
		Last Modified: Tue, 03 Feb 2026 06:21:58 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a48a74ecaa3faaf547586c66a3de9e1445d989a663f5468deadcd301502799`  
		Last Modified: Tue, 03 Feb 2026 06:21:58 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d1624942688f0094bb39b74284bb681745c72ad1d069270d454ed79a85b5aa19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311333267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a206225fbe0eaa08918a5062f432dad69623dcc86a14879a429497dbfeb0d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:19:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:19:47 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:19:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:19:47 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:19:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:19:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0d09fedc597d50c51b783248064f187bb8343caf7d13014c82c7cd9e66241`  
		Last Modified: Tue, 03 Feb 2026 05:20:14 GMT  
		Size: 86.5 MB (86506924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a2a8a6cfc628c3f67b49421d89d0e853e9d214495c3cea23b3d909be150cb`  
		Last Modified: Mon, 02 Feb 2026 19:26:36 GMT  
		Size: 88.4 MB (88375700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c020d175dfc41379afec7f05433bf9bdc194b73268c9aef5d12bbc72d61fe487`  
		Last Modified: Tue, 03 Feb 2026 05:20:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:67470654ccbb6a5327559c94235760e94bdbe7a8e60b0bbbe4b6966b5240823e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a819dd7a99e26c883f2b24636be940af8937d023798c7cbb4e683efec064aa`

```dockerfile
```

-	Layers:
	-	`sha256:bde37a93e8baf0081a145b0b557896f9ac81bd122d707ed0640dcaea16fef6a6`  
		Last Modified: Tue, 03 Feb 2026 05:20:11 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f69d0cc1d63d332275d6c6db61727d31231b6e6771f1447c1d050ce5d284fd`  
		Last Modified: Tue, 03 Feb 2026 05:20:11 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:a106f519fab1bb5b84cb952ec99328241c5f758c641d05748ee2582c44473b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321840607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7649f6b5c23822bc9ae6e3b3ab2277eb9d88bd596253b9a037ef367675d9e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:15:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:17:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Feb 2026 05:17:09 GMT
ENV GOPATH=/go
# Tue, 03 Feb 2026 05:17:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:17:09 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 05:17:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 05:17:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc15e0cd687cd62190081200fbe30ab5102ae840cc68b0386259c387aef2b9a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 66.2 MB (66234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48b8b836d6fc47bc3917c821118f73d4095d609c07c44bf5d9fd6c332861e66`  
		Last Modified: Tue, 03 Feb 2026 05:17:35 GMT  
		Size: 89.9 MB (89859094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4604cae1ff047094cf665f2719aaf0543d71e670a699786143900320f6ba300`  
		Last Modified: Mon, 02 Feb 2026 19:27:18 GMT  
		Size: 91.4 MB (91406236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19252b45be1c7687f9048ba81e7f87930e3cfea2c5a3aa1fc0f22e36c115fdd4`  
		Last Modified: Tue, 03 Feb 2026 05:17:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:83a1c1209dfbfe6dd034709f66e9e1688551f212364bf14584edaa7c6d656d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575a8ffa2e5fb2664579036f385058ff729057bc643490a69f79c17a6bf2f45f`

```dockerfile
```

-	Layers:
	-	`sha256:5e26d242e212bd4743fdf9f01df0b3323acbe136ff601da99a13befabe2b448c`  
		Last Modified: Tue, 03 Feb 2026 05:17:33 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505cfb299293c0b969bb15fbf98e5e3a990c0bb9d7f558f41b18da60c0c67cb0`  
		Last Modified: Tue, 03 Feb 2026 05:17:32 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:109c3c74e34d874b558f2f084cd0ff9e9c1c8a43e942751e2f8e962ba336b800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292896196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e9d4e815b9dd4bcc4a0bf63b2908443bd7b7748cd6e6479022416f19dcfbae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 21:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:46:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:46:15 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:46:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:46:15 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:46:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:46:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:17:52 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee435e05dd9c53ddee45b81a8f55939374cd926a0e00239c752bb0832a5f8b`  
		Last Modified: Tue, 13 Jan 2026 21:22:59 GMT  
		Size: 63.3 MB (63309962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659edd573efc55ccb964dda4fd8e0b2b02903c5753a704b10ec114e6a6fa5f32`  
		Last Modified: Tue, 13 Jan 2026 22:44:42 GMT  
		Size: 70.0 MB (70021799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157797dc2f6c3541f0822449f50b56e0defbd8252c357837e5e2f7b0d8595cc`  
		Last Modified: Mon, 02 Feb 2026 19:48:25 GMT  
		Size: 87.2 MB (87186232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bc21594b1919e5901d0bc94a1d933d1f17b9ba3744949cb7d556efc2bfbef6`  
		Last Modified: Mon, 02 Feb 2026 19:48:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b8cc893c85620f2cc0584d4737c446775214af9a082a03ca5cc18923d7dccd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6453cc45714fe08fea8b61429f82a70d4580ae84b3d994691414bad55e8a2c62`

```dockerfile
```

-	Layers:
	-	`sha256:5291c06ab707b06ae3d186ec9a0f272d429e2e63d06d411dc4936b64b512a91a`  
		Last Modified: Mon, 02 Feb 2026 19:48:16 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:771938ae398c08bb13a8db64d3cfbac6b13ba9f6c254c60f4946bcc79bc3defc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328280506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1655b89b042f2239b0dfd90471ba610813ea5eac861ec6d5fc7549f3181adf4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:27:20 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:27:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:27:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Feb 2026 19:27:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Feb 2026 19:27:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:30 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fcb80ea7d84a82ea96c11045a4f40d0943808d5c5334ea90de2f7ed44f4c4`  
		Last Modified: Tue, 13 Jan 2026 06:38:28 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad800b9fb12dc603a2d36278d51ca7b66bd4da61c9d057c04efc15a63405e8`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.4 MB (90428888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e432b6dca22e637a3a25408001c269ffda0f2c5d9306b2f7174d2a31051778`  
		Last Modified: Mon, 02 Feb 2026 19:28:34 GMT  
		Size: 90.0 MB (90007365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3cd8f45024cbdfb4cc5b9e4dc9514bdbab1462877d936e5fc3db66c9576c7a`  
		Last Modified: Mon, 02 Feb 2026 19:28:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:76d22a03a1084fb635e8371f26259305c28eb4076e54dba986bfc89672f01d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a31269912588509045b584fd27209fbb73795fd9e1491c27254f6f20b09d5a8`

```dockerfile
```

-	Layers:
	-	`sha256:ea3f8afcb5cf17908bf06a7901ffd5960b40bff10752f236ae4c832221dd19ec`  
		Last Modified: Mon, 02 Feb 2026 19:28:31 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28dda92bc5f0769225eab3482afb67e844b67ae6f8644b3ad78acc940195575`  
		Last Modified: Mon, 02 Feb 2026 19:28:30 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:c69fb74779cd578a04f0fa84db7b6836eb9ed47ed4322f73c566939596dfbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296262646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9cd32492f3ea07b875b7248c11cab6d8573c8c260573dcf195f5e9ea038ed7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Feb 2026 19:29:01 GMT
ENV GOPATH=/go
# Mon, 02 Feb 2026 19:29:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Feb 2026 19:29:01 GMT
COPY /target/ / # buildkit
# Tue, 03 Feb 2026 08:58:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Feb 2026 08:58:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed33b56c85899c1cf962e6995242864b8e86ffe5adfb45db579f323fbff37c`  
		Last Modified: Tue, 03 Feb 2026 06:16:50 GMT  
		Size: 69.0 MB (69018751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7062bfc50107a913a5fd7c0d090af1366da08b74147cf71ec4490488730775`  
		Last Modified: Mon, 02 Feb 2026 19:29:23 GMT  
		Size: 92.6 MB (92570442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa05d252fdc57c01848a8098a4623eaf94707a50b58f986656bfe64e68fc375`  
		Last Modified: Tue, 03 Feb 2026 08:59:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b0f91c01c8c837f346850b978b4efc83dc2dc336644b6ed95e3297ea616e7343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7f39320121476806e2ec27e80d4dc280d237699728574da687e01208f1c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:4de7e743a8f64e69c33007e0de63f3a75364735b3636fb4a62d7ea1f23b82552`  
		Last Modified: Tue, 03 Feb 2026 08:59:27 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea024918c7cc0dfd2f1ae6f57bc1a32a1fc23ff40c9d13de3053dedc43bd2fb`  
		Last Modified: Tue, 03 Feb 2026 08:59:26 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
