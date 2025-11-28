## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:edb0c941528b9c8bfbb6a1fa482f0f5f1ae301e2572f450c19f373cbe5ca834f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:366043713c7e6c0f03a9162bdb0a9e212e53a24123d07737478413ab4748d081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60181684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92dd0de9504e0bbe4409feadaddfb844ce08396abb0240bbc740a26215a3273b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:25:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a49a253a05dd471c0e155f0f4f91ccc25fc59aa6c7bd527b323117b5250122`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 11.6 MB (11588572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f16a4357781996ad9405179bea144b87856496993b9d2465452eedb14b76c8d`  
		Last Modified: Tue, 18 Nov 2025 05:25:53 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe7c5d321e038a5990a22a2794a9547dec8a5799070ae3bede181248aee6b3`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd9cd7a5c6fc267eff9196ac84bf0b83ad2ae80012b3d0bed5097cd7ce35a60`  
		Last Modified: Tue, 18 Nov 2025 05:25:52 GMT  
		Size: 89.8 KB (89776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f6ab5e45c7d79f972e35364b00e1e85380de600340204f791446433806794927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c79d811b1da0bdc1d1993a6713d5f35d3b1fe5ddb60cd02a9272b93c89567`

```dockerfile
```

-	Layers:
	-	`sha256:d4326f39e0f4993ebbeb784b9a60db70483b40b2a3fe5331c79ad0b853782ac9`  
		Last Modified: Tue, 18 Nov 2025 08:08:33 GMT  
		Size: 3.6 MB (3577401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727dabe4e2300565ad3af0d1d71e64f1dc685726f00be034d66a37cccd3bf876`  
		Last Modified: Tue, 18 Nov 2025 08:08:34 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0240320d50e0a735877ce9c1b680fc83383e5270c5252f3c5a6bf75773613d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f450dccc1910f9ea53442d037d9c07d6ea9730ad8afe22c7e145b5abbaedbbae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:54:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e8cb6f2050f012301a38350d5b24e1d46c45d720d48514c166af2fa18ea87b`  
		Last Modified: Tue, 18 Nov 2025 03:55:06 GMT  
		Size: 11.3 MB (11255308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12dbc4a5a7d2672202d31ee9d7b29cb5d29a06f08566f247a363e2a63cb672a`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccded1fb17ef0c142f8ae7bf64a99b345608c6adb5b81d14998da21c5d8e1a35`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b042a4e6d45996fb48df60228a59d091830538e87ac00c0c3658e24d51ff587`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d3b1559336fbc2de9e0c6065656e01b75ce0df387ba7457fca8fe58753121d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8978b1b94f45f5e132e11ff42fb8cdcf5277ac0ced6a06a87f419ef33bf4098`

```dockerfile
```

-	Layers:
	-	`sha256:b86a5b4eac17beb5568c3a961e76e6ffd482a8fc5ec835e684237bf06a5cb8c3`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 3.6 MB (3578277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1379a897c2fa408e0db91fe9afff334ac85006ef732f63644534ff4740f523`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:9366598d8a26fb7d7dd14cd014de708e079a3f843b4c78957d0e2679eae472a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61659763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db37c76901f7f42765728dbcbe87d2e8d8ca7d08fa2840b5a41eed82241f696`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:03:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:03:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c99ed386714c4bb450506732ee810d85aab0f3dda4715c62ff3e15a4836519`  
		Last Modified: Tue, 18 Nov 2025 03:03:26 GMT  
		Size: 11.7 MB (11734481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fa4cd2f7a74e88e9df00cae2773c07d4f1b3ca5896efea246d4fc9c3d3b3fe`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5326d561abb9377288ec05ed7812d09e6ad68ee1ffc3de192c6f36932e161aec`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d381cf813812673b11780614a577a1610403eacd68b7a3a520cf58035f4591`  
		Last Modified: Tue, 18 Nov 2025 03:03:25 GMT  
		Size: 90.1 KB (90139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2496c2ba33112048fbc1b81a7e227709bb6d6dfebe4a95a1255c75d60b255087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0158a608fc9a1d83a4d807ed24061af7eae148722c2b6ee838a398f41eebdc4a`

```dockerfile
```

-	Layers:
	-	`sha256:509c1cfcd262c48dcd9ba2791f9f220ab486ca9b0d97c7c174a9264ae3597447`  
		Last Modified: Tue, 18 Nov 2025 05:09:20 GMT  
		Size: 3.6 MB (3575364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf47288a7336f776c2fd7ef0a4483fd2b5da91c83ceb5d5ae52968a4d81d32e`  
		Last Modified: Tue, 18 Nov 2025 05:09:20 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json
