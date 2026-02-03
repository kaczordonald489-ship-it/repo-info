## `emqx:latest`

```console
$ docker pull emqx@sha256:eb2c1bdcc7b102b4cdcbf256c31befe481dd0a29d09e0945f0aa421b878ec898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:ea34a13a728018d841f7edc4cbda5cdcb5331a457cce6237503e9a82ad790096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108402174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263a25cdaf72b3b8752c54d21305c75356b1392dec5b4fe0646379373896e55d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:23 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 03 Feb 2026 02:16:23 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 03 Feb 2026 02:16:23 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 03 Feb 2026 02:16:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 03 Feb 2026 02:16:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 02:16:23 GMT
WORKDIR /opt/emqx
# Tue, 03 Feb 2026 02:16:23 GMT
USER emqx
# Tue, 03 Feb 2026 02:16:23 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 03 Feb 2026 02:16:23 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 03 Feb 2026 02:16:23 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 03 Feb 2026 02:16:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:16:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c830ca1944e25b0d2be37751d4581570c9c6a18bc9c4e8ad0079a1fc1c1f57c`  
		Last Modified: Tue, 03 Feb 2026 02:16:38 GMT  
		Size: 78.6 MB (78622514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df2653b127619f9bd51e422dad8dc8172297cf01ce7bb24323c111ee8c2bf30`  
		Last Modified: Tue, 03 Feb 2026 02:16:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:4af07bff575174ce2067a7dfd008b4e4f50b902b1ad8ae8eb84b819fd8df5f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce64324bef7ce28453096eb2122feb1a5a2f7008cf97cdf3646356ff41702f49`

```dockerfile
```

-	Layers:
	-	`sha256:f6fac9a8b643789f4bdd54fab508ccac188679c2613fdc347a5705dd3d53a513`  
		Last Modified: Tue, 03 Feb 2026 02:16:36 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda53eff9846f7a1b55e47777951f7a554a7010f8aec28fb8b00ad201a7af530`  
		Last Modified: Tue, 03 Feb 2026 02:16:36 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ef0085ef2a4ed2d0b938161f32e62cface85ac5c3fe6c4d977270f0665848a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ca4d711abae686652b330d74dd2bb37ceee00fd0574f1cab1eedfc80f46d95`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:38 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 03 Feb 2026 02:15:38 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 03 Feb 2026 02:15:38 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 03 Feb 2026 02:15:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 03 Feb 2026 02:15:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 02:15:38 GMT
WORKDIR /opt/emqx
# Tue, 03 Feb 2026 02:15:38 GMT
USER emqx
# Tue, 03 Feb 2026 02:15:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 03 Feb 2026 02:15:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 03 Feb 2026 02:15:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 03 Feb 2026 02:15:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:15:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fa985efbab07c388e759fa1439623d387afe308c6b9cd88f535704a215c771`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 76.5 MB (76529559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7a0cf0bb66baaa5e4a60a91efb0798960fcd8dd50fb01776635d8539ec406`  
		Last Modified: Tue, 03 Feb 2026 02:15:51 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:864f6ccfb265cc0aec8899d6be2fe64a67a3b61f10ba37a4eeee2276d0c1834e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b08d838f018ae86a1fba363716fee3917990030eee39c9a254f85072726a3`

```dockerfile
```

-	Layers:
	-	`sha256:28a051599cb0fafb49a9a87fde6f4fd9225cb3ae49afc6cad1e1c5eb8aac7b75`  
		Last Modified: Tue, 03 Feb 2026 02:15:52 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792db421ebde6968ff396aa82bfe14fbfa242dd69bbc9c07ff65d1737cb6d9bb`  
		Last Modified: Tue, 03 Feb 2026 02:15:51 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
