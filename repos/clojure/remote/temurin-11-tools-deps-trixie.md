## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:409766cc5503649d207842e90c38ff505dd5dd5011643fc26c1604662eed9190
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:67a459b3e90fd7b353b26612d43f96956af69c6659f7245584286933fadfaa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279802662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e21857e4e0635567d3e457aa3dd924b18c06af79178d6beea049ad43128150`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:19:49 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:20:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:20:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586c2f1503a6927150a2ecd56e4ee9a21f3aa9eaceb74f6739b344505adc89ed`  
		Last Modified: Tue, 03 Feb 2026 03:20:31 GMT  
		Size: 145.0 MB (144966607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658d2357d95b9beacaf322ba96abc027eb13694522ebed33beb700f77fa534a7`  
		Last Modified: Tue, 03 Feb 2026 03:20:30 GMT  
		Size: 85.5 MB (85542456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2846665d4480ca5a4551a5fa4e1c28c6961661c994c108c34af6fa0a0c1f91e`  
		Last Modified: Tue, 03 Feb 2026 03:20:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7b93bba7f4142ab76a1051237bb79da3d860e171022e60176716dd88862d4c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b8568746c86af65cbca0200859fd5a2846a9364670a99b27b46ac5f364ec52`

```dockerfile
```

-	Layers:
	-	`sha256:655892149e0eee83f4eb975bfec0a0d98784e46b70c888fe1fa44c203b4fdedc`  
		Last Modified: Tue, 03 Feb 2026 03:20:27 GMT  
		Size: 7.5 MB (7487967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6855ad01cf65b56801797b45af6b3761d20fa0f56705506b3b2ef774e76fa2`  
		Last Modified: Tue, 03 Feb 2026 03:20:27 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8aba6e34f0f94cd7a83407afaf7b014bc60f62c2b78b34d2f9aa1031629fb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276743743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c73bbe0bf421c0f3cf954284d421ad117c92acce7557a3f7fe1d018e8f15b7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:24 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c0bbf6cb91a6aca274791498a4f3f1294e4071d6ea4df96a407abdd260af3`  
		Last Modified: Tue, 03 Feb 2026 03:23:04 GMT  
		Size: 141.7 MB (141729907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53faabd019a77daa1df57be55e151deb72fb5f85253a8b5c40c65b1e0c576f03`  
		Last Modified: Tue, 03 Feb 2026 03:23:03 GMT  
		Size: 85.4 MB (85361170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bfbccf1730f5a749c6b654d76f3d0eb7ef27a494b6018ddff67ddb5db2e2ba`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:124601bdbf2ea731aaec8bad0c2052b17ffd438ff58f03e43a2ffe8875ff08b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293b7bd1a6ef87a2e60f8e22204596dc873d00407f822e028b68e661ff39c2fd`

```dockerfile
```

-	Layers:
	-	`sha256:8a8ae27f9e0e19ccc05fc3653daa25e195e8e47d5081a2d263dd88291334c91e`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 7.5 MB (7495615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f7adc3334bd489cb0dd57c23bdb782359aa2d4c9d6c38b7db479896259fb91`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ae431fc64cc3dcc7572b9d32373ba748b6a4df7fd7b3bbf54ee349dec6094783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279340092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb904712a3333e37c6e49ea9a32d546954160ffaad2bc37f5138a230bd25c7e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:20:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:20:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:20:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:20:22 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:21:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:21:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:21:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50438e71707d989ddaa5d0fb396447216e15c2ae0f9452eeec43515a9f6530f6`  
		Last Modified: Wed, 28 Jan 2026 18:21:51 GMT  
		Size: 132.1 MB (132079785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200bb210b9acdbab268c1290ebeb76c906d10d29461ec5bbbf5b8bf2f3d489c6`  
		Last Modified: Wed, 28 Jan 2026 18:21:50 GMT  
		Size: 94.2 MB (94152699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf2277115d14d1c373e2f5c941d939c637febaa76f035162fd524ff4689e4fa`  
		Last Modified: Wed, 28 Jan 2026 18:21:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f27de240d25b0145e83104d02f768e01156b526eaceced473cf692daec4f9576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8512ed1508d8c923adba115169e32822cb9da6802e3dc0f24c2edbafd6308a86`

```dockerfile
```

-	Layers:
	-	`sha256:01d49ed29b065ef542e9a8b73d9ba0ee29a9c02d44a2719381dbc3e90753b44c`  
		Last Modified: Wed, 28 Jan 2026 18:21:47 GMT  
		Size: 7.5 MB (7491773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f1893a81d6045453b56cbe84ada671ed60874615ab041b09128cdde013d32aa`  
		Last Modified: Wed, 28 Jan 2026 18:21:45 GMT  
		Size: 14.2 KB (14231 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b40a6a1195636ab1dd35b72253d3b618bfcce1c484d28413e9dcf604c62bb8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261561436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7210fcd52a96e43c259fb143028282c3342cd42a5db6a386cc4962826803b2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 04:59:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 04:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:59:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 04:59:56 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:01:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:01:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:01:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79570d0434267dfc1c3c1e2bf2c0aeed5bd16edce07420e924b763e62dc668`  
		Last Modified: Tue, 03 Feb 2026 05:00:38 GMT  
		Size: 125.7 MB (125694888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5872e8367e9e81779b16552aa60831f777ea79b60444fb24816c52fcc9aa56d9`  
		Last Modified: Tue, 03 Feb 2026 05:01:42 GMT  
		Size: 86.5 MB (86511524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c8371eae7f7afb748510853405af12fba13516ca06149506dadcd6939faf56`  
		Last Modified: Tue, 03 Feb 2026 05:01:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5349994553170b0f98c2fa4eef4869cfedefe0067812e0c09f2d1a9b84800ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ad01efc54b1ceab1a0f8a5857a1bb01cc16132cbd5f446019abdf789b2dabc`

```dockerfile
```

-	Layers:
	-	`sha256:7f9795c3811359d8bf9e2e35fa9cd3206d1710ea731cfa15d805c93bd42af3e9`  
		Last Modified: Tue, 03 Feb 2026 05:01:41 GMT  
		Size: 7.5 MB (7483893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2931f12f56f46bcc053ca620f641eb1204121237255e95dc9e95b15b0524eba4`  
		Last Modified: Tue, 03 Feb 2026 05:01:40 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
