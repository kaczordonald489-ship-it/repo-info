## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:ecf5d3a8e3633af98e6e4e1294719a121d279c5b0038cf7d889f28b173b941a7
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

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5b9b10fca2d15920abe5c60e953f6a5217c8b8e92447fde88ea4cead4dd4842e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124275691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c598910ab243b3525605244c6fdb3a0b6eb3b5ebd701f29d9e8d26e96ee2ed9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:10:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b6134fa8a3ac5c0189f873bc3e294ab88c8b51487dbaf69fa8590338d4f47`  
		Last Modified: Tue, 18 Nov 2025 05:10:17 GMT  
		Size: 15.8 MB (15764186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01293af2d4fcbec34a6cc04059bc54793a02a3f35097767fa8f319055caf4917`  
		Last Modified: Tue, 18 Nov 2025 06:38:35 GMT  
		Size: 54.8 MB (54755074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee93586b3f25565c44ba18861b5d4d2de6e00ff8473245cb023f5e473d7c9f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fc7b162cf7d5c25440906e9c806e04daec1de3b0a3458dd831c240dbeb3461`

```dockerfile
```

-	Layers:
	-	`sha256:770680dc00a49f18ceccd88f171df69d1645b04ab4e3eba91282770bee89cfbb`  
		Last Modified: Tue, 18 Nov 2025 08:20:50 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de33c9e48b1095ae0c9eb151b841380b3890cd093d27e79382c3970fb670ac2e`  
		Last Modified: Tue, 18 Nov 2025 08:20:51 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dc33d3feecb16f40a33f6dc194b3bad611554ad8358852a05ec7e5d191713e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114555288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd36ec9ae511234a34747ffc8132674648637ec88b947a43f230b79ea3def12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:516616c63b11e5af36116ed0b70c230c2287eab3b74b11a00eb299cc4575af64`  
		Last Modified: Tue, 18 Nov 2025 01:14:16 GMT  
		Size: 49.0 MB (49046365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2280342788a66a44d1f2e4bd1eaf8389d9bef9428e09fa0ae948652bfaeee4b8`  
		Last Modified: Tue, 18 Nov 2025 03:58:13 GMT  
		Size: 14.9 MB (14879454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f566f1ab80bd353b42ed837b52fe4ec496dfff10630b53797d35c9eb72bc27`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 50.6 MB (50629469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d47a2b133e819f63c26775d67970e6d08e4f96cb2e4ceff06a2d347e7d8facf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d346fa15a4de7f828745d5041e61406c0c3615d70219d420bc59a795d8a396`

```dockerfile
```

-	Layers:
	-	`sha256:92751f0bb1f3210c4887a17295e3475616288853442d2f1628a6e012e04ec535`  
		Last Modified: Tue, 18 Nov 2025 08:20:57 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1713120038b26d01d3b777857fb816527979fc95a2de2fb79b0f4853f7ae831f`  
		Last Modified: Tue, 18 Nov 2025 08:20:58 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a401bf4b641e22e520a19090d9c1a6030f332e788960946782813a54dd9e965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122872410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3767701de2c13474cb80279397bcb95789ffa2cf049323057e5f13ee53d21a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:23:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf5c6e26abbf2d346305acdea26f4c77227ae8be9882711816b29b75df95827`  
		Last Modified: Tue, 18 Nov 2025 06:23:37 GMT  
		Size: 15.7 MB (15749561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbea18607285d70f010e2ba402394373534fadffb00b880a34f03b4cba581f`  
		Last Modified: Tue, 18 Nov 2025 07:15:27 GMT  
		Size: 54.9 MB (54865154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0bf9ae62037b2cef297bb2df1a8ff626b25de7c06ddbcf65db81ea529e319333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7264c8438a593a5e4b3cc3c762e5c544554d55a8d536db62ffaa5dcd03a42d83`

```dockerfile
```

-	Layers:
	-	`sha256:131e7bbd66753faac369474d2905aa6c790ce612a47bb99556f512418bd47df3`  
		Last Modified: Tue, 18 Nov 2025 08:21:03 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d4810189770dade5d488b2ec8443840ba17d5798c74320862d6b3f6cdb81a4`  
		Last Modified: Tue, 18 Nov 2025 08:21:04 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9f80cc84eb55cbba7fcbbb9de3012cca5df48aa0e2c401c8a0be5bb626e4eae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127016262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1f4ce8aa2518b9144f21dc990212954baafbc817402ce186ae73ffbeb5b6c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:56:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:09:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91162d93e41e901767fb0ecc9c7694fbbb7b80a5384451f5ee29e2889d7672be`  
		Last Modified: Tue, 18 Nov 2025 02:56:26 GMT  
		Size: 16.3 MB (16267715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d157624c72b4d56de915d1a1b7dc5753760ddee0f8443f1fea29deb51353623`  
		Last Modified: Tue, 18 Nov 2025 04:10:00 GMT  
		Size: 56.0 MB (56048948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:187a1980941fe99b63962633c44a80d455a4beef41175dfb69639bfee267dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a745b457304cf89ed4df90418b5026c5032755869e6e12acd5e661fc087c53e`

```dockerfile
```

-	Layers:
	-	`sha256:0b36d5e29e6878f2e26268d9906598b873ae584c820fccec2cf33f7a9e22f1f9`  
		Last Modified: Tue, 18 Nov 2025 05:22:46 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad162aab16d29fef4efa2e926ddcfda9636bfd8ec13431ec042fe59ef0d49609`  
		Last Modified: Tue, 18 Nov 2025 05:22:46 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
