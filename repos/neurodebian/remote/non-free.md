## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:006ddee33bc319d072a14cc4d994bc2ecabbee1b0945976e1df7658fb4255fed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4c13946a073d0e0d9f2340b836b54e9a9dba1f010f04df5dd200dbc7b1b5af23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59820236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c689286b6669d33d79af74959237011ecd70075c64056e24a6d02c270876d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:51:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:51:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:51:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba456ea91fba33b0b2266f0965cf72ec30eb7f1d6c06aa2a1c64acb11287462c`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 10.1 MB (10073826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c8707cbc6b46ef363481729ebc07a939af077bb4b56fc62ac5a4ff2270d3b2`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba3130f7897eb800b59a9393f231600424ff257e4f3e7b2648b3541566c64df`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc4bfaf80cebb772173dc6b7ebf4d6c65aa74b8a1100448ee711a7b11f0f2e`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 91.0 KB (91037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db51e8517172f9d697f6dd3dfd52ed53bc5d6102dfde87d9d7b154e3f0f1ac`  
		Last Modified: Tue, 03 Feb 2026 02:51:47 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0bb841aee3fa661b5cf22150ac560131f548d1e2f6de469929472a1cae8d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad53c32ccedf0d4c008cbe8f0cc3fa2f71fa4b95414674e681a85c5e5b8f37c4`

```dockerfile
```

-	Layers:
	-	`sha256:130d559f8c021baf79e6466c9df7613170e752a7e5cd42a30367c9f470ca7e5d`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349032d3fccfe1a4b3f53e519f7c3f349aaa60303d81e595a5a2f73a422d2b63`  
		Last Modified: Tue, 03 Feb 2026 02:51:46 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1b7cc3e8e887276f4b47a7a7f3fdb6a9d8ccad482d37c05d554655857987d25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61365948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a8a124a6dc9a583795fdffe09999ff8fe4b6724e1f73ee53a9cc663d7baf26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:50:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b536877d3c0a030ad79a6593cd07fd6d9d694a4ee908632c85159f47caa880c2`  
		Last Modified: Tue, 03 Feb 2026 01:15:09 GMT  
		Size: 50.8 MB (50805135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151531fafaa44052b8ef62edab30c39e82df6362c327e633a87856cab112f38b`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 10.5 MB (10466690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c46322ddba400bbf437e7982be185466ac3a30b6c3e18306fb107df084ef6f`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2601d6950df113d96bbe256462649bc0356027670c0fdeeea1a36db50b8070d6`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbc29155f72161458e612a5e0f3deefd8c0b90f6c6b725d755d6cbb64fdaeb3`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 90.8 KB (90767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a58325440b9ddaee417a935c1ba847b99eca4326d8cbc0cfb83ad3ec4e62d6c`  
		Last Modified: Tue, 03 Feb 2026 02:50:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a1c6b5b1309c9a6d397be72aec7d51df19e72b1ed14d8e559ddaac54b8d45a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834635029b6ce5298f9a745d504c4600d908f105eebe44ef56cca8eff573a1f3`

```dockerfile
```

-	Layers:
	-	`sha256:baf157ba5397d5cc0efb14f1b4af8b0e255ff3dcd41813d3551db6e42c9b6e1e`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190165ca7a14affd0179a3d6aa5c67852f9eccbb4f971c73979a03c8629c2d97`  
		Last Modified: Tue, 03 Feb 2026 02:50:40 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
