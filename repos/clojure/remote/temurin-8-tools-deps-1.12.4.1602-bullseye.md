## `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:270b69e3c6a37b07457b7d7bac8d9b6b4148259993dd0582cb1f0109a0dc0537
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8ae126c6bdb3e8df548d22e1438a26bc84172bf0e492c15ffac3a6b1ffa33a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178031960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de2dc812b6e3b3f2b365177bf668c59031d3080f00ec8fe3730e17cc02b8da7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:18:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:18:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:18:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:18:23 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:18:23 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:18:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:18:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d2deb6b74b92c95615399fc354081905a08d4f21533d6beeaa8c95ebf15ff0`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8908402052550b6a4f420a7ff2e6a75148d81dda741efd8dc17448f9b365f915`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 69.5 MB (69541684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1da291c044eef0710ac68993de2bdb4f3d7f9d664d71da465a57b6cfcc6e01`  
		Last Modified: Tue, 03 Feb 2026 03:18:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1e26edf451b3389677f67625318dd76266e6e81ea7892e067f49da3d2ed845fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7532270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fb7178a71bafee5af6fe50d36548fea7e6f19694e1f0c860b7f8a04a75d2fb`

```dockerfile
```

-	Layers:
	-	`sha256:f4e8c68a2570352cec3cb1f739d18b46897c1b0a8c560caed7c34b0b4983cf00`  
		Last Modified: Tue, 03 Feb 2026 03:18:54 GMT  
		Size: 7.5 MB (7518076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c116cab2040bfbfaff2990450379350e9fd20b1e98fb600ec060d46c2257e111`  
		Last Modified: Tue, 03 Feb 2026 03:18:54 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:916eddfa3ab7c06db4c6d3a8f6c233ac1318b0e4ff21627a6af23d0baefa906e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175767443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd40b53e6d6e637bb0e71cbbd3e69f6dffaa0d229a8615e43bd026a5fb71a4f0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:20:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:58 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc249381c7c21e71287c821a7e215a42dae495893191d56432d1b1827c7c9a5`  
		Last Modified: Tue, 03 Feb 2026 03:21:30 GMT  
		Size: 53.8 MB (53814986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269e53d44fc53d89245ab94fad204377401e5af745eb2400047b6725fb9a8046`  
		Last Modified: Tue, 03 Feb 2026 03:21:30 GMT  
		Size: 69.7 MB (69693491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd2bd1480dd8ebadb762ac76ec9847893eccb74bc1b42ebf5420fc92fa0ad6`  
		Last Modified: Tue, 03 Feb 2026 03:21:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c0f1267ad3b0bd3cf7698b5cb22afd40fac321e1215430118b43adbd43c2ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fb5f8c5ffd8abd4aa326b325782eab3118faf1afe7d7de034b667d2027e36d`

```dockerfile
```

-	Layers:
	-	`sha256:14422de454d6bfabddf07e6006563dc364e18e6943f6a37273ac6c2f676e258b`  
		Last Modified: Tue, 03 Feb 2026 03:21:28 GMT  
		Size: 7.5 MB (7523873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7aa67a12599f75e2c74ef1cf3804633430743bb5fc6766fba141d680287e95`  
		Last Modified: Tue, 03 Feb 2026 03:21:27 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
