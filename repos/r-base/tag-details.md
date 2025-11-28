<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.5.2`](#r-base452)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.5.2`

```console
$ docker pull r-base@sha256:da074726be7a54aab4c49b5f2fafdb464b65ee55d8447d51181793f9cf371a0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `r-base:4.5.2` - linux; amd64

```console
$ docker pull r-base@sha256:5bd6c64ab8057962bd54576cc4ec1494cff6e0496f69409ceb55d52a81a36b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372460519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841ecde3f502255d90fb19aa3fb0dc37c9655dc58d7e8f307cb276b6a89ff0c7`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 05:02:28 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 18 Nov 2025 05:02:28 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 18 Nov 2025 05:02:36 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:02:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 18 Nov 2025 05:02:38 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 18 Nov 2025 05:02:38 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Nov 2025 05:02:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 18 Nov 2025 05:02:38 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 18 Nov 2025 05:03:24 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:03:24 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a9f04603368790b1114219c73b70b85fe6a8ccd82e5a3648b0b0ccaeb92a19a5`  
		Last Modified: Tue, 18 Nov 2025 02:33:33 GMT  
		Size: 48.5 MB (48500435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894753086bc20fb301b1524aa9cee0724809557a20e686d0a00c344d57c556c`  
		Last Modified: Tue, 18 Nov 2025 05:04:18 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7fc381decbe0d186a71e0ae65d86c986a0f6da14c7c69ef785a184131ce5a`  
		Last Modified: Tue, 18 Nov 2025 05:04:21 GMT  
		Size: 27.0 MB (26994630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c089975ddd825a37747c39b96958d084abfa4d1edb03ddc6ae98cf6bad1ae52`  
		Last Modified: Tue, 18 Nov 2025 05:04:19 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf12af43d43d1212ee04f5cf21254d5e81107d659e13294bad6646bcb319377f`  
		Last Modified: Tue, 18 Nov 2025 05:04:19 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca9709d20f1fb897abe7c8242c6be347e1db5548e331f92b486f400bb42ee8`  
		Last Modified: Tue, 18 Nov 2025 05:23:07 GMT  
		Size: 296.1 MB (296093306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:86679eaba23ed3a5f0ee49563366114cb6b943d3094986d42d3ee3d71df58a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12961208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b244210fec6053b2b98797c693e0b41c2dfbd8e687bc76a59b14082dc6cb01`

```dockerfile
```

-	Layers:
	-	`sha256:9f9ac6d5b18f7453060e3255e95b1d4f85203517bc9e65213431f850ad888d24`  
		Last Modified: Tue, 18 Nov 2025 07:16:32 GMT  
		Size: 12.9 MB (12943110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5286a5c71cf69ca337dd7854b72aad7f8b5afe1e47f5406ad13db6e58428910f`  
		Last Modified: Tue, 18 Nov 2025 07:16:33 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:fc9100da846c1c69a485c444e5577f777c7c7982116aae5fa5aee90481820e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353536072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b04685b1993ec52110c4f6dc9a551e1637d6ca2416a1076535cc6fa8d22aa4`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 03:08:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 18 Nov 2025 03:08:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 18 Nov 2025 03:08:12 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:08:14 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 18 Nov 2025 03:08:14 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 18 Nov 2025 03:08:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Nov 2025 03:08:14 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 18 Nov 2025 03:08:14 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 18 Nov 2025 03:08:57 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:08:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f49467d8cd4539a9c64ea7b5c2157fdb7eda1d57099abd6444b4b6f73295cf55`  
		Last Modified: Tue, 18 Nov 2025 01:14:22 GMT  
		Size: 48.6 MB (48591185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b83cb73fb14f21e031741f7863baa9d388839efab12eb37151ef38e3726d3f0`  
		Last Modified: Tue, 18 Nov 2025 03:09:49 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b71cc83a3847885fda328e77ddda81d98924948d905da2a6fff686c5b5585f`  
		Last Modified: Tue, 18 Nov 2025 03:09:50 GMT  
		Size: 26.8 MB (26849717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ba7e5da22dabcd75c814ae0059dba5eedc5f559e981d8f5218343643a17590`  
		Last Modified: Tue, 18 Nov 2025 03:09:49 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981c9d5627ea04b2d36bfad34a1da18a599e66a0749563774264d4d86338ac4`  
		Last Modified: Tue, 18 Nov 2025 03:09:48 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543d89d727238dd758b51876406985a00fe544d96184dfa0efea8970b8cc974`  
		Last Modified: Tue, 18 Nov 2025 05:07:22 GMT  
		Size: 277.2 MB (277223022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:ef4924cf26dec5c5b0e6bd2fa60f7bd833571b4bb329d64a738c87dba71c946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13050454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a9a7f78c6d587841f2e60a2c6a7bd3b94938760bbd43af3f8ea6e935ce529`

```dockerfile
```

-	Layers:
	-	`sha256:6f1898da33e9add34afdf8c80f8636198150c408b3d5b2edcdab74cb9d365afb`  
		Last Modified: Tue, 18 Nov 2025 04:15:57 GMT  
		Size: 13.0 MB (13032216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1141b5c352210dd79a8826c91ba2c1e43fe3a385976eb4ababfa438a3fa00040`  
		Last Modified: Tue, 18 Nov 2025 04:15:58 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:494dfc2a85b63204a3450fa8d9d6c9a857fd2202d0feaca75f1127f95bef7aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364708441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014f5d020f5c5039d4b847bcca25ea85d6118dc24957e5f15e1b78063ee77dde`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1763337600'
# Wed, 19 Nov 2025 08:09:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 19 Nov 2025 08:09:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 19 Nov 2025 08:09:55 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:09:57 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 19 Nov 2025 08:09:57 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 19 Nov 2025 08:09:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 19 Nov 2025 08:09:58 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 19 Nov 2025 08:09:58 GMT
ENV R_BASE_VERSION=4.5.2
# Wed, 19 Nov 2025 08:11:57 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:11:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3415dbe8c9fa5c426374b6be2cb753ee1cd73c4fc4d9120de95ac3d35fa936f1`  
		Last Modified: Wed, 19 Nov 2025 07:09:23 GMT  
		Size: 53.3 MB (53334633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee15d7328451f48b518c9e137d6488124f54bbc898fa6c6dc9161eb590a2727e`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b6e66dc83eaf112b2bef24c190e1faa0c272fbb867c3d05d70f7cfe91133fb`  
		Last Modified: Wed, 19 Nov 2025 08:13:34 GMT  
		Size: 27.3 MB (27280799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec65360ce90369cedde9dd388bd067e37397bb4c202ac6c7d5b2605a53ecd20`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729e10c5c0f3b7dc8c2590a669046fadccfc6136278fefc060fb7c428418206`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8f7be0cae17a1aa67b20839b83bf9ee19e0c42ae1668a14ced35e906eb2cde`  
		Last Modified: Wed, 19 Nov 2025 10:10:09 GMT  
		Size: 283.2 MB (283220857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:0460b7d14ac8a09da35fe672bc13d6971bd2aadb885695714e9d34e2d2b9a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12947036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8cd14b2342ab207bca0f8f6a7cb7521e272de44ec46100ac97f82ef2478bbb`

```dockerfile
```

-	Layers:
	-	`sha256:a40a4fc179c775a9e557cf82472af22ab59f758472cfbcb7169fc23e17ab0d60`  
		Last Modified: Wed, 19 Nov 2025 10:13:39 GMT  
		Size: 12.9 MB (12928899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84dd5fd94dc8d0de837e7f4666728f7c73fe26e0c39a3abdaa288e898f80ffa9`  
		Last Modified: Wed, 19 Nov 2025 10:13:40 GMT  
		Size: 18.1 KB (18137 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:4.5.2` - linux; s390x

```console
$ docker pull r-base@sha256:9532735ee76dc7ff0b5e53d6954719ec8c6ccbfe8e207eabb9b33fed9d39791f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332636197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6ce297eec1b7ed1693256c5cbe2e0dbcdccac09f8d3038f55bf25a91e98ead`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 17:12:19 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 18 Nov 2025 17:12:19 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 18 Nov 2025 17:12:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 18 Nov 2025 17:12:29 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Nov 2025 17:12:29 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 18 Nov 2025 17:13:14 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 17:13:14 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:963b067f9eecc96262cd77759b1e1e10770c29e86028729532e1addf32185ef1`  
		Last Modified: Tue, 18 Nov 2025 16:21:20 GMT  
		Size: 48.4 MB (48370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dea34b0b304b671b1e68ea1b207c737440ae67aad5d87fea93f9e8420dd6724`  
		Last Modified: Tue, 18 Nov 2025 17:14:15 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ecf2cdce502d1692f7146779e4274647b22693ed82609ae90042f0a81e8de`  
		Last Modified: Tue, 18 Nov 2025 17:14:22 GMT  
		Size: 26.9 MB (26940450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bed3a14f9d98c89602bbeb6774bb80b9d7b0452cc722d3a2e63a8a3ab38c8ef`  
		Last Modified: Tue, 18 Nov 2025 17:14:16 GMT  
		Size: 924.5 KB (924544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00846d50bc4627b5d8b632a8ad345b1732ff83526244f1f8d175ce0db34a6901`  
		Last Modified: Tue, 18 Nov 2025 17:14:15 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d5c40ea17843ad266953330db3f2491fc42ae42375ffeb8cf9f689a93e8e36`  
		Last Modified: Tue, 18 Nov 2025 18:36:44 GMT  
		Size: 256.4 MB (256396605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:4.5.2` - unknown; unknown

```console
$ docker pull r-base@sha256:31ccf4a4cb9692779e87d4aaf6b7a56e202041902da372db7eacfe71f439fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12752420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be81ebf30a90d6785fdaf74635f84bc1e1aa73517fed050a95ad5e95a0eefee5`

```dockerfile
```

-	Layers:
	-	`sha256:7498527058ac4d9de775ca551123c7d01493b4ae8c9d92228e3acbbf4fa55716`  
		Last Modified: Tue, 18 Nov 2025 19:14:13 GMT  
		Size: 12.7 MB (12734322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf6d64b58d9193a810329c01ae22c94ee7bbdf8674b057c9aa8a3885b1b3d8c`  
		Last Modified: Tue, 18 Nov 2025 19:14:14 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

## `r-base:latest`

```console
$ docker pull r-base@sha256:da074726be7a54aab4c49b5f2fafdb464b65ee55d8447d51181793f9cf371a0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:5bd6c64ab8057962bd54576cc4ec1494cff6e0496f69409ceb55d52a81a36b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372460519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841ecde3f502255d90fb19aa3fb0dc37c9655dc58d7e8f307cb276b6a89ff0c7`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 05:02:28 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 18 Nov 2025 05:02:28 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 18 Nov 2025 05:02:36 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:02:38 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 18 Nov 2025 05:02:38 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 18 Nov 2025 05:02:38 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Nov 2025 05:02:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 18 Nov 2025 05:02:38 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 18 Nov 2025 05:03:24 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:03:24 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a9f04603368790b1114219c73b70b85fe6a8ccd82e5a3648b0b0ccaeb92a19a5`  
		Last Modified: Tue, 18 Nov 2025 02:33:33 GMT  
		Size: 48.5 MB (48500435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894753086bc20fb301b1524aa9cee0724809557a20e686d0a00c344d57c556c`  
		Last Modified: Tue, 18 Nov 2025 05:04:18 GMT  
		Size: 3.3 KB (3314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7fc381decbe0d186a71e0ae65d86c986a0f6da14c7c69ef785a184131ce5a`  
		Last Modified: Tue, 18 Nov 2025 05:04:21 GMT  
		Size: 27.0 MB (26994630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c089975ddd825a37747c39b96958d084abfa4d1edb03ddc6ae98cf6bad1ae52`  
		Last Modified: Tue, 18 Nov 2025 05:04:19 GMT  
		Size: 868.5 KB (868485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf12af43d43d1212ee04f5cf21254d5e81107d659e13294bad6646bcb319377f`  
		Last Modified: Tue, 18 Nov 2025 05:04:19 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ca9709d20f1fb897abe7c8242c6be347e1db5548e331f92b486f400bb42ee8`  
		Last Modified: Tue, 18 Nov 2025 05:23:07 GMT  
		Size: 296.1 MB (296093306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:86679eaba23ed3a5f0ee49563366114cb6b943d3094986d42d3ee3d71df58a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12961208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b244210fec6053b2b98797c693e0b41c2dfbd8e687bc76a59b14082dc6cb01`

```dockerfile
```

-	Layers:
	-	`sha256:9f9ac6d5b18f7453060e3255e95b1d4f85203517bc9e65213431f850ad888d24`  
		Last Modified: Tue, 18 Nov 2025 07:16:32 GMT  
		Size: 12.9 MB (12943110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5286a5c71cf69ca337dd7854b72aad7f8b5afe1e47f5406ad13db6e58428910f`  
		Last Modified: Tue, 18 Nov 2025 07:16:33 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:fc9100da846c1c69a485c444e5577f777c7c7982116aae5fa5aee90481820e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353536072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b04685b1993ec52110c4f6dc9a551e1637d6ca2416a1076535cc6fa8d22aa4`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 03:08:05 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 18 Nov 2025 03:08:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 18 Nov 2025 03:08:12 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:08:14 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 18 Nov 2025 03:08:14 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 18 Nov 2025 03:08:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Nov 2025 03:08:14 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 18 Nov 2025 03:08:14 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 18 Nov 2025 03:08:57 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:08:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f49467d8cd4539a9c64ea7b5c2157fdb7eda1d57099abd6444b4b6f73295cf55`  
		Last Modified: Tue, 18 Nov 2025 01:14:22 GMT  
		Size: 48.6 MB (48591185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b83cb73fb14f21e031741f7863baa9d388839efab12eb37151ef38e3726d3f0`  
		Last Modified: Tue, 18 Nov 2025 03:09:49 GMT  
		Size: 3.3 KB (3312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b71cc83a3847885fda328e77ddda81d98924948d905da2a6fff686c5b5585f`  
		Last Modified: Tue, 18 Nov 2025 03:09:50 GMT  
		Size: 26.8 MB (26849717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ba7e5da22dabcd75c814ae0059dba5eedc5f559e981d8f5218343643a17590`  
		Last Modified: Tue, 18 Nov 2025 03:09:49 GMT  
		Size: 868.5 KB (868487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981c9d5627ea04b2d36bfad34a1da18a599e66a0749563774264d4d86338ac4`  
		Last Modified: Tue, 18 Nov 2025 03:09:48 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543d89d727238dd758b51876406985a00fe544d96184dfa0efea8970b8cc974`  
		Last Modified: Tue, 18 Nov 2025 05:07:22 GMT  
		Size: 277.2 MB (277223022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:ef4924cf26dec5c5b0e6bd2fa60f7bd833571b4bb329d64a738c87dba71c946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13050454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a9a7f78c6d587841f2e60a2c6a7bd3b94938760bbd43af3f8ea6e935ce529`

```dockerfile
```

-	Layers:
	-	`sha256:6f1898da33e9add34afdf8c80f8636198150c408b3d5b2edcdab74cb9d365afb`  
		Last Modified: Tue, 18 Nov 2025 04:15:57 GMT  
		Size: 13.0 MB (13032216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1141b5c352210dd79a8826c91ba2c1e43fe3a385976eb4ababfa438a3fa00040`  
		Last Modified: Tue, 18 Nov 2025 04:15:58 GMT  
		Size: 18.2 KB (18238 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:494dfc2a85b63204a3450fa8d9d6c9a857fd2202d0feaca75f1127f95bef7aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364708441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014f5d020f5c5039d4b847bcca25ea85d6118dc24957e5f15e1b78063ee77dde`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1763337600'
# Wed, 19 Nov 2025 08:09:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 19 Nov 2025 08:09:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Wed, 19 Nov 2025 08:09:55 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:09:57 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Wed, 19 Nov 2025 08:09:57 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 19 Nov 2025 08:09:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 19 Nov 2025 08:09:58 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Wed, 19 Nov 2025 08:09:58 GMT
ENV R_BASE_VERSION=4.5.2
# Wed, 19 Nov 2025 08:11:57 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 08:11:57 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3415dbe8c9fa5c426374b6be2cb753ee1cd73c4fc4d9120de95ac3d35fa936f1`  
		Last Modified: Wed, 19 Nov 2025 07:09:23 GMT  
		Size: 53.3 MB (53334633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee15d7328451f48b518c9e137d6488124f54bbc898fa6c6dc9161eb590a2727e`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 3.3 KB (3313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b6e66dc83eaf112b2bef24c190e1faa0c272fbb867c3d05d70f7cfe91133fb`  
		Last Modified: Wed, 19 Nov 2025 08:13:34 GMT  
		Size: 27.3 MB (27280799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec65360ce90369cedde9dd388bd067e37397bb4c202ac6c7d5b2605a53ecd20`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 868.5 KB (868489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729e10c5c0f3b7dc8c2590a669046fadccfc6136278fefc060fb7c428418206`  
		Last Modified: Wed, 19 Nov 2025 08:13:31 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8f7be0cae17a1aa67b20839b83bf9ee19e0c42ae1668a14ced35e906eb2cde`  
		Last Modified: Wed, 19 Nov 2025 10:10:09 GMT  
		Size: 283.2 MB (283220857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:0460b7d14ac8a09da35fe672bc13d6971bd2aadb885695714e9d34e2d2b9a9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12947036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8cd14b2342ab207bca0f8f6a7cb7521e272de44ec46100ac97f82ef2478bbb`

```dockerfile
```

-	Layers:
	-	`sha256:a40a4fc179c775a9e557cf82472af22ab59f758472cfbcb7169fc23e17ab0d60`  
		Last Modified: Wed, 19 Nov 2025 10:13:39 GMT  
		Size: 12.9 MB (12928899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84dd5fd94dc8d0de837e7f4666728f7c73fe26e0c39a3abdaa288e898f80ffa9`  
		Last Modified: Wed, 19 Nov 2025 10:13:40 GMT  
		Size: 18.1 KB (18137 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:9532735ee76dc7ff0b5e53d6954719ec8c6ccbfe8e207eabb9b33fed9d39791f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332636197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6ce297eec1b7ed1693256c5cbe2e0dbcdccac09f8d3038f55bf25a91e98ead`
-	Default Command: `["R"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1763337600'
# Tue, 18 Nov 2025 17:12:19 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 18 Nov 2025 17:12:19 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Tue, 18 Nov 2025 17:12:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 18 Nov 2025 17:12:29 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Nov 2025 17:12:29 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Tue, 18 Nov 2025 17:12:29 GMT
ENV R_BASE_VERSION=4.5.2
# Tue, 18 Nov 2025 17:13:14 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 17:13:14 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:963b067f9eecc96262cd77759b1e1e10770c29e86028729532e1addf32185ef1`  
		Last Modified: Tue, 18 Nov 2025 16:21:20 GMT  
		Size: 48.4 MB (48370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dea34b0b304b671b1e68ea1b207c737440ae67aad5d87fea93f9e8420dd6724`  
		Last Modified: Tue, 18 Nov 2025 17:14:15 GMT  
		Size: 3.3 KB (3316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ecf2cdce502d1692f7146779e4274647b22693ed82609ae90042f0a81e8de`  
		Last Modified: Tue, 18 Nov 2025 17:14:22 GMT  
		Size: 26.9 MB (26940450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bed3a14f9d98c89602bbeb6774bb80b9d7b0452cc722d3a2e63a8a3ab38c8ef`  
		Last Modified: Tue, 18 Nov 2025 17:14:16 GMT  
		Size: 924.5 KB (924544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00846d50bc4627b5d8b632a8ad345b1732ff83526244f1f8d175ce0db34a6901`  
		Last Modified: Tue, 18 Nov 2025 17:14:15 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d5c40ea17843ad266953330db3f2491fc42ae42375ffeb8cf9f689a93e8e36`  
		Last Modified: Tue, 18 Nov 2025 18:36:44 GMT  
		Size: 256.4 MB (256396605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:31ccf4a4cb9692779e87d4aaf6b7a56e202041902da372db7eacfe71f439fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12752420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be81ebf30a90d6785fdaf74635f84bc1e1aa73517fed050a95ad5e95a0eefee5`

```dockerfile
```

-	Layers:
	-	`sha256:7498527058ac4d9de775ca551123c7d01493b4ae8c9d92228e3acbbf4fa55716`  
		Last Modified: Tue, 18 Nov 2025 19:14:13 GMT  
		Size: 12.7 MB (12734322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf6d64b58d9193a810329c01ae22c94ee7bbdf8674b057c9aa8a3885b1b3d8c`  
		Last Modified: Tue, 18 Nov 2025 19:14:14 GMT  
		Size: 18.1 KB (18098 bytes)  
		MIME: application/vnd.in-toto+json
