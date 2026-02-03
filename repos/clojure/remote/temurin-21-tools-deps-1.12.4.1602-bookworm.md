## `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:8abe2f86523a18bcf0db4b0db35c9aeb2ec06d7f615563d5bc07310c5d9ce4a4
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

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1805f55149ff182a48686c7ae6359460e1b20585f837cf9bdf1fe292226869ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287459020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224a3a86a33fce7f169af0c9470adde512602630fef1dd5add96b1f355705eb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:21:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:21:42 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937e2d1283a8c329565703daa764cb33d8bb0cf46a66a2fa58a71dacd14cda61`  
		Last Modified: Tue, 03 Feb 2026 03:22:23 GMT  
		Size: 157.8 MB (157826065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e4353a57e328058ff4882192bc27b1f84b37636fefa458eaf8deaf40a1d6ab`  
		Last Modified: Tue, 03 Feb 2026 03:22:22 GMT  
		Size: 81.2 MB (81150429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dba2b363aa243863d2ca1e4da70392e293fc44368d3d4f609d98c86265a4fb`  
		Last Modified: Tue, 03 Feb 2026 03:22:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052aef3c46b01371cbd82467bb0872a5a70fb158f17161b61f36fb353eb9af97`  
		Last Modified: Tue, 03 Feb 2026 03:22:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b03fed5038c0287e216dd65414c86ce0e1c61738e744bd37b2b90ef465d45368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0840f887ef087bbb0a2a267fd76eeebfe93ff3539642378b35b22e04c7b5fcfe`

```dockerfile
```

-	Layers:
	-	`sha256:f271ccd00068be46fb99e5fa82b436eb18f8da9cd75d5bfc3d1d44c4dac22c38`  
		Last Modified: Tue, 03 Feb 2026 03:22:19 GMT  
		Size: 7.4 MB (7379323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e7c62ec8cbc10187fe299c913139d0630758001c92b3687eb36683f2b6f591`  
		Last Modified: Tue, 03 Feb 2026 03:22:19 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f065a4bd3716d25f71e137833fcbe38c665a5fc6ddebba9f2d809bdfea1b896c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285612910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ddb8e2e157de290a646aadd884cde358420ac861017ba85a0a05865f2157e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:24:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:18 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9063cd0c133dacfac08e0fd4e25f3db9b28b1f539eadb4fd6d283ea07587e7a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f49315398e8a542cbfcbac1a7d3bd7d6152de5f8e8d9838de23c4d2c93d293`  
		Last Modified: Tue, 03 Feb 2026 03:24:57 GMT  
		Size: 81.1 MB (81138331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e140930bc4d67530071a0e003116200e183b3db3f350b569ed0fd3c83cb4f5f3`  
		Last Modified: Tue, 03 Feb 2026 03:24:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f805144fc079157afd830db753eb7518a063a90f3d6469bb572cea5aa30e20e3`  
		Last Modified: Tue, 03 Feb 2026 03:24:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:acd04cda8aa8c9ac784a3eafb00449b64e041716a45ff5c16d39890a4bf7a435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8260e4089c3bacb91991360b9aeeeca9eb14aa8553eb195de61d7972319f28`

```dockerfile
```

-	Layers:
	-	`sha256:a9d34b38f9badb67e268e1961aa4c2c157315a2a408f8e03393a52d05a63aaae`  
		Last Modified: Tue, 03 Feb 2026 03:24:54 GMT  
		Size: 7.4 MB (7385110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6a8a055df1c89ce5e2dbd0d14ae118c11d47d4cea6c761b5cbf8ee7d363fba`  
		Last Modified: Tue, 03 Feb 2026 03:24:54 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:31d938a04798d7e3509b5153420c4129103e89a8d67609b21ebda91630dd0e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297258437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb295ac0e57f81e6f4024f96611789ff29029e6e892008430bcc955d805b841`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:26:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:26:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:26:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:26:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:26:59 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:27:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:27:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:27:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:27:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:27:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3edee8149cf4bfe2bdf95487958a292e196ba2b723670ee4a4e1e494c9284d`  
		Last Modified: Wed, 28 Jan 2026 18:28:23 GMT  
		Size: 157.9 MB (157942968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decf3715d411e1228584850542c13f35f5582886cf3a94dbe596cc00fc1c246`  
		Last Modified: Wed, 28 Jan 2026 18:28:21 GMT  
		Size: 87.0 MB (86987051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041a0e0383c89680541621dc49121ebaf534665605dcf970acee7c6d2d831d5d`  
		Last Modified: Wed, 28 Jan 2026 18:28:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21076fd1d5d115e3306a497932f5a32f591ac9b742a13c84649fe33d9f0c7dac`  
		Last Modified: Wed, 28 Jan 2026 18:28:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fff281492b10043707927c233f36d2606debbda428f0b0f267e9af39117e7172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca49ad3dc566d16cb815e9aefbcc1be1c34f95098ff6abbb047d94088134d499`

```dockerfile
```

-	Layers:
	-	`sha256:a514158a289df9f2bb370d31edfa4af31c890ad6d0cd6ee145269a6805647c2c`  
		Last Modified: Wed, 28 Jan 2026 18:28:18 GMT  
		Size: 7.4 MB (7384551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de96522f39f12e6ab6d0a412d8acfee513dc45f3f37284cb385275175185603`  
		Last Modified: Wed, 28 Jan 2026 18:28:17 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:53130020b92bcf700019bffcb99218925c9f1ef6637c8ec732a96e85a1c233b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274172476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d65a4e7b8bab5ff8f07d95ff27dc7e1c40feceb6a072972d6603345764b787`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:03:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:03:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:03:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:03:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:03:53 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:05:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:05:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:05:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:05:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:05:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ae753e080cc50ca20884f34f16a7a103d8cdee0bb115b2a6163947581cac7`  
		Last Modified: Tue, 03 Feb 2026 05:04:33 GMT  
		Size: 147.1 MB (147069863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f26cf5e20f2e5a06746f9faa8a1790827a9da5a2b652eb538fded26a86839`  
		Last Modified: Tue, 03 Feb 2026 05:05:35 GMT  
		Size: 80.0 MB (79963225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448155525bbb71c2ab420cf46ac3add1aee314fa088fb0e35e0652469518db5d`  
		Last Modified: Tue, 03 Feb 2026 05:05:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b039260781d6c037e9c41a51a09e75f3cda97eaee55f032d1419b94fa8f132d`  
		Last Modified: Tue, 03 Feb 2026 05:05:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8eac972d47f6ba2a62a4d5149ffb9d73edabedd6c26d5c2848841dcf7863c523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626b354abf8d49974da546b44f168fd9408a2158448a7660d22ef32452eaeba8`

```dockerfile
```

-	Layers:
	-	`sha256:959f0944786b431e162d3099fe15d09c9f233ff9a4858c3388eb08af22b929a7`  
		Last Modified: Tue, 03 Feb 2026 05:05:34 GMT  
		Size: 7.4 MB (7370642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f4503cd662e8860f284722ea8ef5caf4e875bf1fb1eda35bde25eef6ff9122`  
		Last Modified: Tue, 03 Feb 2026 05:05:34 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
