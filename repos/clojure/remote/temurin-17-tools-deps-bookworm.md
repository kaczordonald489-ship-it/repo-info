## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:23d13f22641ddf0b23d7fdcc269779bf1b01e7e09024bc0bd0bdee24b128ce4e
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ebd4dd6f1b0c5e69e296885bad59423cea0b33359f42713f928aff72c90ecc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274480947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e0a81b109189b88b58215252c308957b74ee9832bcb90bd4c89d44aa4a7b8f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:37 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:20:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:20:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11eeebbc3a9877491fcf22b3da6d80dce81b27358f07dd1d4f3fc348e628063`  
		Last Modified: Tue, 03 Feb 2026 03:21:15 GMT  
		Size: 144.8 MB (144847923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6b7391d6c648b4064d755ba7bd7b449a04b5e2e5d14e301373cea3718f2f0c`  
		Last Modified: Tue, 03 Feb 2026 03:21:13 GMT  
		Size: 81.2 MB (81150496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca0b157f41a6fd66b5518dd4915da971707b510cb8fdffd5972adfffdf94d2f`  
		Last Modified: Tue, 03 Feb 2026 03:21:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ce4999532148e2db15f15ce2dcf3619f42270af5b376d24fa2c84015f32fe9`  
		Last Modified: Tue, 03 Feb 2026 03:21:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5711a231fbc0a707a9e98e2a0fd5da2418c245b1a6c54957aa11b10fd1b6fb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e1889b7b253d080a51134b584482eb2fd4ca70e379f752d2aef7839e8db317`

```dockerfile
```

-	Layers:
	-	`sha256:bec2e40454fb732d0934d870927a0f11905fad315a9cec770d7c895793652f68`  
		Last Modified: Tue, 03 Feb 2026 03:21:10 GMT  
		Size: 7.4 MB (7375537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db4a96f844aa69f6c25950cf9fe86907439e9c536ad62291078187675a9e771b`  
		Last Modified: Tue, 03 Feb 2026 03:21:10 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d31642645eeb76dc3858061c5828609a005e6f75eeb3211d14e6c017bf0f5e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273185613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55399e314acfb2a0b60abf4b3dc2c19b8dfdb34133d838e56db0f0b681f63298`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:23:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:02 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e68f6ea6e1a1cc07fc4589b035e5077bbf7845126457a3ad80cb0b786642c1`  
		Last Modified: Tue, 03 Feb 2026 03:23:41 GMT  
		Size: 143.7 MB (143679941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9e7a7da6991b84bb7e632f45cf4812b8ae4e7842416320ef31bc9787857656`  
		Last Modified: Tue, 03 Feb 2026 03:23:39 GMT  
		Size: 81.1 MB (81138674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e11ed63f744c3ca36dcb5ad1cf019742728322017a5301730b32c2bf322707`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec4deabe2dcd10185a09d36e242dec6c0a9d40a3c4f4a0f7bac63c361530609`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4f266d2657eec45b61934a18619b15b3dd9759c44f7ada4d9d4ee9bb881e7baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111a1a49c89b4dd3a1f2b52cea1e75f5d23f68ef1659f690ac9bbce1c9076730`

```dockerfile
```

-	Layers:
	-	`sha256:69b2750262fd83b03e6d232a5831c84a34200c00c026367ca5d93ed359e08d76`  
		Last Modified: Tue, 03 Feb 2026 03:23:37 GMT  
		Size: 7.4 MB (7381300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb856db7dfdb7df36a5857528e3e9a2c3e812dcdeee067726d7c622f1e802ab`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:4931bf0ab59fcefacfce0f0325d84ded5722232f48cd4bfda9025663a1ee05c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283840639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c4b330d37d4b6e1e8e346b48b8425e2d98a696e80c063ec88564bcb8782fab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:22:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:22:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:22:08 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:22:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:22:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:22:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:22:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:22:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fbee1bb403f77f615e65138a7f3f83ebbdd41dcc148d0618e1d492d141013`  
		Last Modified: Wed, 28 Jan 2026 18:23:34 GMT  
		Size: 144.5 MB (144524725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aed2772937e06ef8ad39137131fa3872ce25c75f49b5977e65da267f08ef80f`  
		Last Modified: Wed, 28 Jan 2026 18:23:32 GMT  
		Size: 87.0 MB (86987498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a860611d7ed451d3edd579af643b62cf4bbe7f573a9c5c36804d279ed3f796b`  
		Last Modified: Wed, 28 Jan 2026 18:23:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cb8035565c9b7c6a8165cf7239ee5b8e88ea6890360e2607bc7a22fe83c746`  
		Last Modified: Wed, 28 Jan 2026 18:23:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2a04516cd2b4c5dacd45c2727d90ae1ffa4776e83e568a1a997e3b2e82ad4934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adcc959e422be2d619ee4225a8a8ce65bb8455a51e12154dce34ca7b6cedc95`

```dockerfile
```

-	Layers:
	-	`sha256:992114c1b48c4f07a1f1766cd318b11db77b9ba6f24b3b4200e8622c634848c9`  
		Last Modified: Wed, 28 Jan 2026 18:23:29 GMT  
		Size: 7.4 MB (7380753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf79b47b14cacff4a373bf59288bc60783cb151aaa677d7f5a5307d73a14ae98`  
		Last Modified: Wed, 28 Jan 2026 18:23:28 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:5772b6629c35dcae31fc10335a7002ccaeb7e6b34daef233e00ec0cd6938a47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261962175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b37f3210f9498c77aa85d3614670997177af8257f56715f091330e240d5136`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:02:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:02:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:02:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:02:48 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:02:48 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:03:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:03:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:03:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:03:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:03:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757fa1c248d50fc3a7243e75610057a293d6d883731114d2323093252fa19ac`  
		Last Modified: Tue, 03 Feb 2026 05:03:29 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413593e03f1e508eb4b06babe0c2aa39bf8dbc89536f5b2539f57457fdaf84da`  
		Last Modified: Tue, 03 Feb 2026 05:03:31 GMT  
		Size: 80.0 MB (79963017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882c36fc83e705b69fdf37e17c0b04bdc617a4c8eea75682e374f789e65f585`  
		Last Modified: Tue, 03 Feb 2026 05:03:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f83b3d028871786de55e5231f7f6bfe351b6408fe7df55d434229262b5803`  
		Last Modified: Tue, 03 Feb 2026 05:03:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:73091dfe20e2862cc9603cec4f06bde43dcbe088a6017d4f3083def81e087239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1abe5ebc6368cf8a30b4fb31935865e6c2865b70daedf367afa60600152705`

```dockerfile
```

-	Layers:
	-	`sha256:67b006aa7c6aad1dca0e4beb4700d97f806d3be76002a2b2d585607e6b748ccc`  
		Last Modified: Tue, 03 Feb 2026 05:03:29 GMT  
		Size: 7.4 MB (7366856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebba98bd5e8dad9aa5ca0127bbdb286eb635762c27f49dba733ea3cffa6431c4`  
		Last Modified: Tue, 03 Feb 2026 05:03:29 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
