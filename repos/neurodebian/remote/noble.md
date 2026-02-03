## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:3b1ea9866549892bcfb5deacf0a8f1dadf9c2f98bc63ce01b622f7745ea46c65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:39dab19ea0056fea381a2e3081c573bfd689d2656f5cc81fd3aa41ae0aafcc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7aa252972df966e8bf224240d541b7d88ce8370c9fa313cc2adeea313cf30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febb96c351dc6c0d19a074b7bf0a980146f228694ed515a5e6e4776348b5d83`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 3.6 MB (3563150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad77fe67014a99e49ccbb36bfa471550dbfe256c0a7997b77cc92db588b238`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d558af79b48a1dc1eba2fd55a45ab5177f557780a20b8afd5fecaf034f577cb`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c341089aea08830c751d3756d07510e12c782bb60ddc69ebaab8ffa5029a30bc`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 104.6 KB (104575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a7b83fa45a2ec02faf249af7419c07420383708eb87fda857dbfe98bdaed5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3607dff0dabf71a31ae8a8d3b3a75f55737f7a69e1d3dc070f88269b85f1486`

```dockerfile
```

-	Layers:
	-	`sha256:d9ff96588e736f2de78e48e58e17efe725819c5302f84fabc2e05fe87cbe845e`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4dd02fcbaa60ee0e870849b37cadc44a2fc95004b2b0c366e2b4f9fd44b22`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bbd6e0261957f20c46d34962987746d93400c15e314c81f6a64419c91b7b065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32532687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eca9e911f1ef800afe0cd19724f336ae82260d50c9f4b9f782df0356d4b3c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11d827e327f828ef515a5ee3828fc7df7429f4b6fbac0be158005236e186fe`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 3.6 MB (3560792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e9075292abfb37049926dd278eaa023c87947273bac27af654d465972b0ca`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a28cca6467154fa487391fafc9c46ab2569d2510dcce267c204dcd1149a12f`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7e1041691204d39dc1e2e6b9a0d184d8a90b0de7386c680d0babf4b584849`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 105.2 KB (105161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:48009258df992087de7fb120477a38bf8c9e7890ce32c805c7f253896db012ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e121faf012875be8415caaaa95813bfc205ab8f562b254334d16b738816f0f13`

```dockerfile
```

-	Layers:
	-	`sha256:f1c64391a4650e5d5a17196f03e5b2562ea6d98a2f0c2f9a560cefef58af1128`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bda8fe80c01c55cfd927fcb6b54d5213dc934c85a38e089a1945a03b8baf762`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json
