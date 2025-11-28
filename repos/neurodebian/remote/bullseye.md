## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:4a17725e892257ad4267fc45a29f31e2c2893d7b34fc4da4feada937b7169692
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:52b23456ab2f9d29fd759ecaf2e5a2541030add2851a9b053a51c2d867599c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7d7b6f18d2ebf89a1081e0b667b4c8a57cd1c4916e28e5a24d831549248bdc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:22:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:23:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:23:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027086a669e3187a5bf55f93556ceea5dd486b73a28bc08d86aeb65a70793707`  
		Last Modified: Tue, 18 Nov 2025 05:23:16 GMT  
		Size: 11.1 MB (11105091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d191edd77c0ae59bd17b0f6640a0bf2d8749774ef5877ce401308fc7547fed3`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18651e8f324fcd83223a52a2730112eef035e1ceb11219aa7de401d66434f20c`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977616fa4c9e859613cd50ad00c392b3a050ff5e4a7cef8078fad26854d79113`  
		Last Modified: Tue, 18 Nov 2025 05:23:15 GMT  
		Size: 101.4 KB (101405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f3d82782aafc3fabcb0f4cd571387f5f0469eef5209184cb44f4f03e814e201a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061182ed89de96f15a42206b239284ea10a77684e0117e45c8c83a75cee0bd5`

```dockerfile
```

-	Layers:
	-	`sha256:72e2841e7d8a353d852c2136dfde3cbb9389c533a5e49bdf8cd92300794ceed3`  
		Last Modified: Tue, 18 Nov 2025 08:08:23 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db020feaeee2fafa232e497baf959f91c0631ea5ef2f7c8f5db85e3332bac212`  
		Last Modified: Tue, 18 Nov 2025 08:08:24 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7a0e1a673379a86a94d3c2e3bdb42728b33fc4c251ff6891b1acd4a0ee392337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91a451e442d2e4459f8608f6798004fbcdecc5b1e051cc8175efd38e757b228`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:49:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:49:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:49:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:49:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722ffbbe605a785238ffca2eb8744eca1f0f76e1718902782cfa899d81515702`  
		Last Modified: Tue, 18 Nov 2025 03:49:53 GMT  
		Size: 11.1 MB (11106099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fb98ab4c345ad520c24eb6e96667d26e24c539579fc55b995d86777c6bb33e`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea69364ab834cf76a2f1ed7a4892a53173db03de6c6957be53af710be6d154e`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc8a13c0c8e09eea2ec7010f3f7c34d2f741e4026897300d421405d259332f9`  
		Last Modified: Tue, 18 Nov 2025 03:49:52 GMT  
		Size: 101.1 KB (101107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3130883b211251a00c8f3138872d2127f486ff9b84eb8de852200a2db4de557c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5b0b8e3b177bd5d484e96e7564af795d83a58c23b9e5d5059342292132fca4`

```dockerfile
```

-	Layers:
	-	`sha256:4dd6ac5ab9c023c50b5e8c1658a66a76ee36f0f03532fa710143b1b133af7592`  
		Last Modified: Tue, 18 Nov 2025 05:08:59 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ca9c35ba0c1fb4e0e1288a61902514b9b4d9045956de4d3b40fe5fa9dc8ad9`  
		Last Modified: Tue, 18 Nov 2025 05:09:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:5aa69718f1efaca3418c6d918472ccc3610a069dad9a5de8dec3ea485a595596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee264702ebd5954f33c687a868e40ef83a54e39bb0fa536e18202657530adc9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 02:59:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:59:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:59:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 02:59:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff276d829f31f5253bbd1b7f53ddf75bfd6004f7fcc06ea8ad1b23a242b12d3b`  
		Last Modified: Tue, 18 Nov 2025 01:13:28 GMT  
		Size: 54.7 MB (54699599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad6c4930bd9f54fe6d2bb6d571f25016096ca17f5042810bd28ad8cd30e0587`  
		Last Modified: Tue, 18 Nov 2025 02:59:20 GMT  
		Size: 11.5 MB (11500406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e6ed60e67a01f2bd9eb7737b35f9071edcafffa6a7408cae777d51d9aa773d`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69b163bcb414900c226707b4e354f29cb924661cd161524e15552c784f5b6c`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ee899bbd601f3a72f64d5c1253c7739d0a559b58cd7d06c6c3fb6f3699916`  
		Last Modified: Tue, 18 Nov 2025 02:59:19 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31e9b963b769aa8402cb4f8e020e7d2d926e8589b11ccc0473e774492f589e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0865b8f651164a8cce85f937a8680f329663d66744888c46adf7d5ffa95c6c9`

```dockerfile
```

-	Layers:
	-	`sha256:ee00c44865291a391a9bcaf7b8de266296f6f9be6aa7c0b628ea626c63eaa1f3`  
		Last Modified: Tue, 18 Nov 2025 05:09:04 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108db865401eccf5faad0834934c22e016bb182f2028e5f435587351e58dc2fa`  
		Last Modified: Tue, 18 Nov 2025 05:09:05 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json
