## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:99748e3801a87ca4754f030cbe146f3d2d61e73399fe09d89e6d2fb75c3ff494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:feaed26b03c949d0932e37e6e74f547fa6f99ad36f56d1aaf9574b4303d94193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567098fb1b1386891c3045fa629bf7193516c5be3c1e7ea4583b46e9f125f01e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 05:25:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:25:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 05:25:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:25:41 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:76694dc296168bbffa890c84fb372e9c250bf33e0ad63a6146b169a57d983e2f`  
		Last Modified: Tue, 18 Nov 2025 02:29:31 GMT  
		Size: 48.5 MB (48500434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6f932371b762d4ebd76295ed523041ce96b651c8d6f99058e56fde0193577c`  
		Last Modified: Tue, 18 Nov 2025 05:26:05 GMT  
		Size: 11.6 MB (11588603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95424eca70e0b48eb1362dc9faf54d6cf60c34acb74bebc377ccd001eb0a5b`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751758c3326f3120503e1065f2ee9d96dab1645821c5d9040b49ea54b7e4b182`  
		Last Modified: Tue, 18 Nov 2025 05:25:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e407f8ac8dd6b87d5030356d06d625859834a1b2fadc44b8b309603476fa0b3a`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 89.8 KB (89813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bf0c4c970ca715981804e3d2797bc8cc57df79fc87b3e0d8f079f416f688ad`  
		Last Modified: Tue, 18 Nov 2025 05:25:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dd9844cc45fbe3e9de05e6c77c740d47a5f577608e3b189b07fb86b1cb4ee288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85735ebb9f37ee391cb4778514b2f1e223e828f04d47c74fdf38f6a08dde99c8`

```dockerfile
```

-	Layers:
	-	`sha256:938f600c2b882bab1eac886bc2abee6d9baca24359cb1c9bc53463214580ac7d`  
		Last Modified: Tue, 18 Nov 2025 08:08:40 GMT  
		Size: 3.6 MB (3577437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cccbb40e13d48227175631b605120ebd5591330729672805e5b424dfb34585`  
		Last Modified: Tue, 18 Nov 2025 08:08:41 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:64186adde6428fae5c84a5002a30127063d0e3db638a8e2a0ecf21ba6744d014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2540b57cd8e8582e9238a43716c2655c40d1d64033d51b15977395dfd3a37fe5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:55:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:55:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:55:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:55:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:55:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7442761efa65f5c2b8ea533bdf899a42a7675c104757f17e02556f4fb8e9b1`  
		Last Modified: Tue, 18 Nov 2025 03:55:30 GMT  
		Size: 11.3 MB (11255244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48646b8eda1068da8aaed34b5cab1846deb098a42975c11138a3a5949dbf2b40`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eee381d7f6529a319746474450b633a97370dce62728e2ef7ad068a023a2f2`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7d4af7149a94e629b6505577fcbe8866b4bab79ca6f413e0a47f39515ac258`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6cdc60206bb5f64f8f48ac0b1ada92e0746562966eb4588e033f00586bfff1`  
		Last Modified: Tue, 18 Nov 2025 03:55:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e70f2997d786cd98e0bd721ece2fe2b7fa22520c9e84c2a97875debc9767eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6882a6e3ee02ae9ae4109396d8e989351a7877d8e2876e150ad3670ced3c95`

```dockerfile
```

-	Layers:
	-	`sha256:4d89ca1be6665cdfc905578b87af2c5bcc78c8cbab78dc211a784b9f6e401e1b`  
		Last Modified: Tue, 18 Nov 2025 05:09:24 GMT  
		Size: 3.6 MB (3578313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c76a11b7847af5b890757dc45a0626a35c12771f24ac9352bf5efbde44662bf`  
		Last Modified: Tue, 18 Nov 2025 05:09:25 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5af48f027b4bf48cdee6090d22551922b9a844d5d5a07910d479a440e699496a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9346116137dfaa71689745f00f12a0b4289514a6e182a2e5ca85439dd3403175`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:03:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b6295fb3a0de9675da59780f9f04f82fb6dcdc2676ee484a93d1d29644c69`  
		Last Modified: Tue, 18 Nov 2025 03:03:50 GMT  
		Size: 11.7 MB (11734522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d910717d3eb8247dc5797a539a4501e15f2baabc57447b9e40100725d7bf149`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac3671e7d327a12e834092b1f44ca16784cd66ea96c40cf45f0398e1b99af04`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f22aff5a131d31db729bd6138d046dacb2be96f9ded5b0c4d416274d261cdf`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 90.2 KB (90163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a543a8735d0a34b0f63dc1dcaa2ed6d8f2db203b8b5c1ee2d951c571b57353`  
		Last Modified: Tue, 18 Nov 2025 03:03:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0f6863f842eabeed89212f42d99ec2925a2ff7a135b4e11706b9828510aa27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041d6b5f4b3615ac3cd6a4e876b23a9a9d37bb780b40e3482302391c9b87358`

```dockerfile
```

-	Layers:
	-	`sha256:6f42b733b57f390b5db85df406b02ab8db246d4befc1ad0cc48b1305eb6d15dd`  
		Last Modified: Tue, 18 Nov 2025 05:09:29 GMT  
		Size: 3.6 MB (3575400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d1f5346f232ba860339a91bb3c9310d60c2691ca72115e3462cda0ecdd79d1`  
		Last Modified: Tue, 18 Nov 2025 05:09:30 GMT  
		Size: 15.9 KB (15928 bytes)  
		MIME: application/vnd.in-toto+json
