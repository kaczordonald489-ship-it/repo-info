## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:1436dad2e58bec97423fa2590a88d20cc88555ffa10aca1bc28ffa268b9d43e8
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:77308d9aeaac0849012c5a2a2ce1a67cba3639fdcada559c61dd700ce6edfa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279684188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432caa8483055ae053a77c11d61089f6823db3965c335318ba69e09473b2912c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:52 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6b5ccad96566173b43229caa3526f8d98067f8d2d3abf1223de66ebd02e5a9`  
		Last Modified: Tue, 03 Feb 2026 03:21:36 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e437a15311489559bf31d5fcf08383cdfb4d3cce33dced587ff64e6bb58d84e9`  
		Last Modified: Tue, 03 Feb 2026 03:21:35 GMT  
		Size: 85.5 MB (85542286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddddf92f3e9c9d880dc286b702ccd4ce70424162e11e6508b3e9831faef5138`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee16f5dc0e7137c908d078bbd959a5e5df69e64a31334b37766aefb392b0256`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa7e14455fd455ea34c1c3b8914e9ece34327e9a71b69a405f66b8a0a0112242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa580b3ee31d816630b42ab9c810c044fc8cad2900f0eb135a51b47913b790a`

```dockerfile
```

-	Layers:
	-	`sha256:0f45fdd2024b07a38bcdd1e079729d851e68a85a6266853fe483ae61870e6ac6`  
		Last Modified: Tue, 03 Feb 2026 03:21:32 GMT  
		Size: 7.5 MB (7467828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420eb8a873a1c73f1fe2d4cc073ad09c6ff7b9a768b9ccfa5f2f33836831a130`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3470730190e0a18974cbe348124ca3fc919f20368cd8eebc2ea8eda972f9df43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278694122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22ac080c201b7fa88daf53157924face58edbf2408d071a60aa0589ed5f8f06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:21 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a9f0a030353240ddda4cbcd483763b021b00b4088b29b17ab8bfb24238bf3d`  
		Last Modified: Tue, 03 Feb 2026 03:24:02 GMT  
		Size: 143.7 MB (143679921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb5d1dfda71e663f7c3c02ef17752eddc6d424e11e0559b6c8844053d3fb9`  
		Last Modified: Tue, 03 Feb 2026 03:24:01 GMT  
		Size: 85.4 MB (85361139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b48dc019008523f7ff0aaaf808cc1ca5543a70f4bb73f8ba1af3d11d3ab3e6`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088fa2c40b1d5e122cd04ee8db1830de236086363891508fc2eea83ab88f28c0`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:71bedf68c074a42371efd16fe60e9f763442aedae62759d0b0d78a36ca1a3a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0464420f45af714186513806e2964f829cf30484f8651ee94444b94a2e0c973d`

```dockerfile
```

-	Layers:
	-	`sha256:8befff019ea730dfee61dd9bc6805786d3973a7a999c6c04073ba401a73c3c85`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 7.5 MB (7474858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29651c02e99a77868e5fa3d13175b851d341e4c38d511c73dc664c5a825e0c8`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:214c9c825ff0da8d7de5f0dc917afaf764938bf35b9ed0ddc166d2105db226b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291785545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41928f8e026bcc166b185c34e4e4e0af57ef5f8b73a6fe69af951d532052db7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:25:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:25:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:25:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:25:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:25:12 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:25:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:25:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:25:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:25:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:25:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1018c3460cf258236be180731a45a091aeea7a0b3099f92e9bfa486fa3b9252a`  
		Last Modified: Wed, 28 Jan 2026 18:26:43 GMT  
		Size: 144.5 MB (144524726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ef909c30e213ea4306a50a74e64036751ffba5581dac282f8c22a46a94804`  
		Last Modified: Wed, 28 Jan 2026 18:26:42 GMT  
		Size: 94.2 MB (94152815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abcce7df5dae969bcb0e81d99bccba0e847d817aee4af55b99dbf882a34b275`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829aca8d3d201a504f4efe367658360a58e65c8fdd41fe21cef7173451a3b187`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:da86331e6713db46463c301a4488b04b05b06a3e9e80ce5e87259d4721fba7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6549593d80e2c1eedeb05c10b8a03c1453c3803653e34ff25c92143592f8ca36`

```dockerfile
```

-	Layers:
	-	`sha256:7e64b9ff682544ff2635b1dfd50388b5953e3580b13dcc32a84fbab85eefc92d`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 7.5 MB (7472249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf198f1b7b0eb1894bce0252727e6c55cb3fea409fbeee03b2186a27c77919a`  
		Last Modified: Wed, 28 Jan 2026 18:26:37 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ee89d285b4169a172a53f40849e97d89c51b69d3445729fda8d4a6350ca724d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270726822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5860ae589ff1016a15e328d259c7c42f1b164461e3588c03e8b6210f4d43cc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:02:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:02:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:02:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:02:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:03:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:03:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:03:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:03:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:03:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0521af9429b24592bd981b694df00f2d02ab05a0bbb63192b66fd3a113c887f`  
		Last Modified: Tue, 03 Feb 2026 05:02:39 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e4bd1e22af93d28689f0ab20120c5927d2fce6f2e55a11c719edc1fbcf065`  
		Last Modified: Tue, 03 Feb 2026 05:03:41 GMT  
		Size: 86.5 MB (86511632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d412261b3b83a828dbb590e4b722bc164306d24e48ad849a2c46308cb348675`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c96c69f0a4832d4fbe8b9f450d66db97b808dbeebfdc1e473778b0f562fcc55`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d40e4b08b2cf917f90b2b5b256779a46507d1a6e81cae55055ee97444bb39024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d015407a3ba71296a11b7c6acb745432f599d6492590c300a84c4172abc900c9`

```dockerfile
```

-	Layers:
	-	`sha256:1d72b51a75250e065edc9e5309261d1f2ea25c5efb6522ad2c47ed4bf77629a2`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 7.5 MB (7463750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3594c17612954abcda742be695766d4e04bb07c5f1ee92737f0ff02184c1248a`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
