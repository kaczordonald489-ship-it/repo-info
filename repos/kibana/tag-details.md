<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.7`](#kibana8197)
-	[`kibana:9.1.7`](#kibana917)
-	[`kibana:9.2.1`](#kibana921)

## `kibana:7.17.29`

```console
$ docker pull kibana@sha256:214fd19f90efd750940e1269ec992f254b641c78b9d8af2a184f84cd4e69daca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.29` - linux; amd64

```console
$ docker pull kibana@sha256:c0aa33485941239d163f432b239d3a02f4df8626f45b39b0637290313baab979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353913008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdd23f0c4a7707dd255886269010b1e12cfbcb4323108633a4dec4424bc098c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:28:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 13 Nov 2025 23:28:28 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:28:28 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 13 Nov 2025 23:28:28 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:32:15 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:32:15 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:32:15 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 13 Nov 2025 23:32:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:32:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:32:16 GMT
USER kibana
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdb63166b01065b5f7b99b6c9aef0b064c2619c8a8d2aa28900c35620dad640`  
		Last Modified: Thu, 13 Nov 2025 23:33:06 GMT  
		Size: 9.4 MB (9432171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0e243fbaf8e56d5b355b644529d3ed4788c625a92dbbbed24fdb160ca65e1a`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49d4ff80eb1fe4f3116402fc8f8b14f01dd2667c426dd0c6ba3a71ed0a4f7ae`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48405d79663978c1cf545837462f1c20b1c07ad7bf145101b7627051b2bc13d8`  
		Last Modified: Thu, 13 Nov 2025 23:33:06 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aa325ed52e36638eeeb312d4f855b884465eb853383b69373091f002014281`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e171d897aa16a8798e29bab0abcec849131cd946dc34713709b638e7c904ae`  
		Last Modified: Fri, 14 Nov 2025 03:16:12 GMT  
		Size: 298.1 MB (298112553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd272ceee08e890fbedfc09bf4dd061bbc4cdbb94d8a97ecdc2026c1ea650c5`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9ab140f6e2dfdf61227617e6a235aa453a7a3f6495115ae02e6fd77406f46`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5b9c0f18f07e84fb9334b4b92b4c3c56b4fd1cf8fa909b539c13b757e88328`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8f438b26057468d57ceec2555726a6b4dedb5198d5a72fc8c9ecd062a05e7`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1b7f1c0d124847f7c8bd31f3a70c1960fffbc81978dca5f157529e7ae128a8`  
		Last Modified: Thu, 13 Nov 2025 23:33:06 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718e8bc690f6e59d6eed6bf905a7b0b1f518eea1b038ab980ac727f64a813b6`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.29` - unknown; unknown

```console
$ docker pull kibana@sha256:4fa9431b42decd61b978c094b1f5167968be0f3cd93303006765164e1eb49fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070f1f745153a061d784200168e4aa7e45a1cc2c84a72c951a3c90a273eb4e3b`

```dockerfile
```

-	Layers:
	-	`sha256:cdfa6528661e2f127de796a7ebba4c0bde44c8f21f0e9b1134614821f5132474`  
		Last Modified: Fri, 14 Nov 2025 03:11:42 GMT  
		Size: 3.5 MB (3506834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57fbad5574700428d9e57e578aa8dce94626a1457e6016765d503452d6e2e899`  
		Last Modified: Fri, 14 Nov 2025 03:11:43 GMT  
		Size: 44.5 KB (44511 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.29` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3304b1b08cd54106bb61c533d80cb4ac4d8ca905abe5351e6eaf1792e8f27762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366095962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be02998de38651cfc11fe55dda0c3b10ea8d6d31ee19df52bf76301cecf9227b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:35 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:27:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:27:35 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 13 Nov 2025 23:27:36 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:30:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:30:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:30:52 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 13 Nov 2025 23:30:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:30:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:30:53 GMT
USER kibana
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6397d3511035aaa5996ddbd63c844242cdf265782c4d0652b67548aa3fef509a`  
		Last Modified: Thu, 13 Nov 2025 23:32:03 GMT  
		Size: 9.4 MB (9446173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1853a381f41232f921e5526c3e6700154b827f6949ce80249b881bc6d699cd09`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a760837544bebe14a33bb967a1935d4a4d15c3abb9227281080d71dbe975e53`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922bd60bd5fec7692b52505f3a4906334bcbb68e40c63f2ec9e47f2af918012`  
		Last Modified: Thu, 13 Nov 2025 23:31:51 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89931a8edb2c8dbee44c71f14803f8136f4ec18de1703d9337b4641620485f85`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf67254e8331c96e4c2f96142859368e57085c91814b2f0e300934367be2c05`  
		Last Modified: Fri, 14 Nov 2025 03:15:36 GMT  
		Size: 311.1 MB (311148121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55926e73b726f9b587823eac64e2486adf2c4bc7eaaf0dc86a1823587916f465`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f1fee166071308bd9f88d3a9c288789bb822f58d513126237e97547bfffb71`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12355655218fe6c3b48187926fe316193619b4b7b9eae9eab2d102d577d00a30`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a729783706fcbd9ef444378dee2624e0fffa33a4213baa8a774ff08d00b3d2`  
		Last Modified: Thu, 13 Nov 2025 23:32:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3565fad2095d35954b8261412110b44af400bcd11be235b398ae7faf5599bc`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 158.0 KB (157999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54760310f932ac7c65ec67da5c9eb6f576c221ed4872eb417a199ea2a76978`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.29` - unknown; unknown

```console
$ docker pull kibana@sha256:8439078a15410074229ad08b9ed26610f0bd8aa625c8448dd6c283f751be204b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe7a100c42b2ea8ceae595e317296dd281ae632807f3d9ecb9cfab35ee560c8`

```dockerfile
```

-	Layers:
	-	`sha256:fdcf66b35195edd1229f8daea36f16ec924ae474f9c9f5d639b1d96a824583e8`  
		Last Modified: Fri, 14 Nov 2025 03:11:48 GMT  
		Size: 3.5 MB (3507898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee98450ea19b52544a490c084455349bf886d683fc7244bef3585fb42d8c9cf`  
		Last Modified: Fri, 14 Nov 2025 03:11:49 GMT  
		Size: 44.8 KB (44789 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.8`

```console
$ docker pull kibana@sha256:4c73f1e8fd61baad0716c71dfedba2194ed909300560ad66ab8251bd7f11ba94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.8` - linux; amd64

```console
$ docker pull kibana@sha256:d7c4b9662d957cd41fcfb32c554cd7c25557899511fb09926fa28156bcf77ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424079670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb990441cddf3619a69ce486f938576316aab79cf986845612b20f00e41d4df1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:34 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:28:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:36:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:36:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:36:54 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:36:55 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:36:55 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:36:55 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:36:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:36:56 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:36:56 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:36:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:36:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:36:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa7e3f5276d9a52d6abe8527fe00e8cb71ba993e041bcd1c37db82c8565f62`  
		Last Modified: Thu, 13 Nov 2025 23:38:07 GMT  
		Size: 9.4 MB (9432182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb566056a2f72f3c0d36be7a38997b8d1d6462fa0ec8fcd234041db225389c`  
		Last Modified: Fri, 14 Nov 2025 03:17:15 GMT  
		Size: 368.3 MB (368279132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddec7aebe1d1a4de4d26a7d08e1a2884cddaaad30f12908c9f66aea29148e344`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14ea6f6f4524247905656484936f3bba1a49c33d1360378e554c90512d922df`  
		Last Modified: Thu, 13 Nov 2025 23:38:08 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1887c4ab1d067a93261b962ac9fc4ee3820741c138017f89775ba504c0c4a`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be88165050c540019b55dcb3913d33e928cdee0c4950798c1cf7d4f067d6d7e`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47beb95e0935f6cd8b92bf84d7fcb59013455e99af72163cce89e37f559ef66`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e29c2f534b0713ae1eec9e185d5ffecdf40705e8627f6ca30fc1ccaab92ca3`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 4.8 KB (4768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3768e40446a0706b1d9c9f95a34b73f1b6453918f88b905d5799df0d5c600ac9`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d1815f836fc48b66044cc1656e343143eb66fbe43e74d8dc8d4f7908b2233f`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf42b8285681325cd51e1d6daff0127a6c5590674382b14d5242e9a185648b8f`  
		Last Modified: Thu, 13 Nov 2025 23:38:10 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:903053e21ac27118b9c5b77612c4294c83d9260bf49800b978739d34ac05c329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db160e71d7afcdf8ed587c1bd01a7ee260c511a6b8b4279380bb10a3f20494ae`

```dockerfile
```

-	Layers:
	-	`sha256:ac2feab0794231218fd3bf52afbe2cb6f36e64a50adb2439190bd1a04bc4dfe2`  
		Last Modified: Fri, 14 Nov 2025 03:11:52 GMT  
		Size: 4.9 MB (4856890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30130bbfba23015d367d7aeab62a8d79e080423b3f708b6eaad4cfa1d184bd66`  
		Last Modified: Fri, 14 Nov 2025 03:11:53 GMT  
		Size: 40.7 KB (40684 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a8c795e0a6448f4112b26df31eab623d233f5d55c2dc9070df3c3313532ad6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.4 MB (436355230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f4e07683e123e4f95f04229e7bbc0322ad90a09a67c5186cdc0cf1cbb4c0f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:46 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:27:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:34:44 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:34:44 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:34:44 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:34:45 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:34:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:34:46 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:34:46 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:34:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:34:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:34:46 GMT
USER 1000
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de63df616becf613cf5fe961e187fc6129aa4b6d1b5509db6b1df0c8855a7a7`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 9.4 MB (9446139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c090a108fe140a15dedec5955270529bff007c1f1c9a79677aa83379c3f4b780`  
		Last Modified: Fri, 14 Nov 2025 03:16:43 GMT  
		Size: 381.4 MB (381407353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7addf77df7fe3204f04de322cf7ea86b59e69c8aa9e26fd50a7d9029226be5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a65f8bbd7e9d95181ae79ffd18b90a44d166c7025a2325e93eb0488cce6d6c`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8eb30e0d24f5bd8f1e55fa2c70d40abeb3433cf53b0fd561aaf5070fe43193`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410b06427c0b5cd07cc2eea851aa0bc7da593c1a21c9c9d673677c9867b1bca5`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cfd7eb4342b3ebb07a436bc7eabb448cfb63b08af09ff8a2a17f506f43da25`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7486155002a8e617ffd5b2f54347df258b3acb32f2c6530e0781d42c4fae35`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 4.8 KB (4764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba29ab01d8b73367d63e6ad72b76b69fc579d73b09a2b157e9c559c2a4389`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e8d5b05c91bf573a0a0ab1ff3ac21ec59e16c1c610d4f760e59c7ae083801`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87df0fbd969ca87b03ee7923e2deb35235ebdf8c4094c4ebc4df8817e742d069`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:41ef8b811dd035e7a1e850902ee962a8c3fe964f8357cc5fb691331bc1f749f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4898884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a87c03b89fd13cfbb2670177deec5a6271f3e0ffc05f2b13e14a0d47e8c036`

```dockerfile
```

-	Layers:
	-	`sha256:85181590cdcb3a32a258d062299c54dacc57f14065bb67bf603805a639544277`  
		Last Modified: Fri, 14 Nov 2025 03:11:58 GMT  
		Size: 4.9 MB (4857954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1dcf166553967c58eae09a06b1350bc953ba549467c61d69fd22deca57c029`  
		Last Modified: Fri, 14 Nov 2025 03:11:59 GMT  
		Size: 40.9 KB (40930 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.7`

```console
$ docker pull kibana@sha256:1d28569d88f6e52e1bfc7f34923f3d24749ae7de6337914ac2dd434f54ec465c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.7` - linux; amd64

```console
$ docker pull kibana@sha256:71dc9196d39832f10a65be18fe65882c59c399e53c4e303944f163b35599243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436690788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238bcd211df399d4ce21b1ef586d31db92c37e1b0782252ad75263e8d713f8ae`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:39 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:28:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:37:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:37:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:37:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:37:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:37:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:37:29 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:37:29 GMT
LABEL org.label-schema.build-date=2025-11-07T13:25:36.883Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28cf679904329ed50de370ff1e1e71f1b57996a1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:25:36.883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28cf679904329ed50de370ff1e1e71f1b57996a1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:37:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:37:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:37:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e831024f1e65cae7c7e27d092da8d03c06d50b739ca11159f3e8d53b4859e3`  
		Last Modified: Thu, 13 Nov 2025 23:38:38 GMT  
		Size: 9.4 MB (9432118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413e3835eb47da03dc335b427679a5c0c4ac7c4656f3a91694507c960744d84a`  
		Last Modified: Fri, 14 Nov 2025 03:18:20 GMT  
		Size: 380.9 MB (380890274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1312679a3caa1156b3e798453d802d7b24c4dc935ec9a998ff6f9664a917832a`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330ec6fad6c2c37195404b82de22ff39497e7759a6be8cefec847cdca64468da`  
		Last Modified: Thu, 13 Nov 2025 23:38:39 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2c3d951f7e8cff27cfba26fe0b8cf04cc224d8165877d5202b39fbee6953e0`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 5.2 KB (5238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2824797228c74ecd81482051326b7dcb654e99a76bb0d63f1a1a6cbeac0ff`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c88815a00e2ee1fbdc6a344b7f496d4886e853d319083fab0ebb4b1fde8671`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839bc2d33d02584c921fe20bb12f648b40663c8a8290077672f6b1e9aeaf4ebf`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f079f359d83263e052fe364dcf95b7000e4bed8da87df76342546dd1c924ea6`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6be2768226b4808616941db3689c7752b7939ba5056bb35a28fc4d12c80d587`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab46a087591e71b2147800a57a15b9fc197c31e3267c6051641233dc4c594ca`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.7` - unknown; unknown

```console
$ docker pull kibana@sha256:7e4b03456994b8e86c5530d2b35a04320c07d31127a3c67d20f5d38a7077d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba23ab72257b4d15ce49bed40726ef9551fe615ca7412146c30b6d6dde57a52a`

```dockerfile
```

-	Layers:
	-	`sha256:9f0671a2e66ed26d9b3ebe2645efd504c35f7c53db5f7ee25da6724c24412359`  
		Last Modified: Fri, 14 Nov 2025 03:12:04 GMT  
		Size: 4.9 MB (4874334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf72418f2f67a4f3983bb9e82c59bc4d65a1f05457bdc1d69c2064cd0f812baa`  
		Last Modified: Fri, 14 Nov 2025 03:12:04 GMT  
		Size: 40.9 KB (40907 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8b82f41480e00f701b5765508bf37f05acb180813f6a84289bff0e8e0fc7fc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448862487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a11b798b164f4d7112d6c0ddab89b520339bab4f687ef0ede47e13e17447e6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:58 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:27:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:02 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:35:03 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:35:03 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:35:03 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:35:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:35:05 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:35:05 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:35:05 GMT
LABEL org.label-schema.build-date=2025-11-07T13:25:36.883Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28cf679904329ed50de370ff1e1e71f1b57996a1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:25:36.883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28cf679904329ed50de370ff1e1e71f1b57996a1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:35:05 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:35:05 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:35:05 GMT
USER 1000
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555b2904321a495d59cc123c17789cb19eb74703f4b76d3a7bbaedefa824c49e`  
		Last Modified: Thu, 13 Nov 2025 23:36:33 GMT  
		Size: 9.4 MB (9446146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f046b6e1f3967f5bd455e37809db07978c1515ed557e31616a7e0de691f23b4`  
		Last Modified: Fri, 14 Nov 2025 03:17:55 GMT  
		Size: 393.9 MB (393914557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7743957bbd66fe2732fd3cc420ff68b980ba95a3f93dbbb428f9fd585348bd40`  
		Last Modified: Thu, 13 Nov 2025 23:36:31 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f6a0f68663a88b3f6a8b77ab28c22040b6456013381c38c977f23be8fa44dc`  
		Last Modified: Thu, 13 Nov 2025 23:36:34 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a810635ed59548280e58ba9230f96a13ab95575aeeafec71206d4fb6ee0dfa`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 5.2 KB (5238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c891093adb2e87e5ea14ca4e1de2766d3f4973e3d210d76924720671b6bec1a1`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400782be555936668c0c0d4abf99eb77523b9104780675655801ec3b2b86e7c1`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd3462599017d3feb67ba7a48e6bef09ea15fdb478dcb6bba9848a9fa63fc6`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9885633034580c4b3cef2c775ce1c6f4ae1569c01145cb41d804dd608788c5ec`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f163694eb13a45e458a441f62fad091ec28046c6580f05a5f9927ce434ff`  
		Last Modified: Thu, 13 Nov 2025 23:36:33 GMT  
		Size: 158.0 KB (157999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af3d90a714fb96f4049a49476b0ee80051cd389bd4cf5b3250292f49c2fd74`  
		Last Modified: Thu, 13 Nov 2025 23:36:33 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.7` - unknown; unknown

```console
$ docker pull kibana@sha256:1bfbbde40adb84f925f2a64ee0154d865384305a54fe9568e4bb3e57b17d3448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4916553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a57422385740c1f9073578caa9727ccec1a90fd2fdc83bda6eebee6d58b142`

```dockerfile
```

-	Layers:
	-	`sha256:90233e5142c3a2ed9ea323b7260be37235810e33a9cc02000d927f1c65fc0e1c`  
		Last Modified: Fri, 14 Nov 2025 03:12:10 GMT  
		Size: 4.9 MB (4875398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1ae6380c0dbe8a2687d4e96f00ddd8d2c30fae2b2e466d49c7d3aa45ace277`  
		Last Modified: Fri, 14 Nov 2025 03:12:11 GMT  
		Size: 41.2 KB (41155 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.7`

```console
$ docker pull kibana@sha256:7286f88dfb9267cf2b094bbf3970cb77a4a21aa29a8b2a78dbe34ab70334e37e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.7` - linux; amd64

```console
$ docker pull kibana@sha256:464e8617fc298c6586a250170c68f329d8475d1439e3c7fcf7d462ed5e96faf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437901192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff3560e8cc2115ed56decbb543f15c3777e2907f2c0b7bd1db54627e566bfef`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:51:18 GMT
ENV container oci
# Mon, 17 Nov 2025 06:51:19 GMT
COPY dir:7cf80e1c5cade8bdab1a4d70632d27e8826f968a3bd11979550b2850547e929b in /      
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:51:19 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:51:01Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:18:00 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 17 Nov 2025 23:18:00 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:26:36 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 17 Nov 2025 23:26:37 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:26:37 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 17 Nov 2025 23:26:37 GMT
RUN fc-cache -v # buildkit
# Mon, 17 Nov 2025 23:26:37 GMT
WORKDIR /usr/share/kibana
# Mon, 17 Nov 2025 23:26:37 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 17 Nov 2025 23:26:37 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:26:37 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:26:37 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 17 Nov 2025 23:26:37 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:26:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 17 Nov 2025 23:26:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 17 Nov 2025 23:26:39 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 17 Nov 2025 23:26:39 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Mon, 17 Nov 2025 23:26:39 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 17 Nov 2025 23:26:39 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:26:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 17 Nov 2025 23:26:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 17 Nov 2025 23:26:39 GMT
USER 1000
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7eeaa75ed3173490d531c2e616e17eb6d385d0d011d6774418885feccb39a9`  
		Last Modified: Mon, 17 Nov 2025 23:27:49 GMT  
		Size: 19.5 MB (19536971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b62970ddbe35cff203bf8a0c5bebb415a081eecf3e6a5e99f2d2f41eaa21fd`  
		Last Modified: Tue, 18 Nov 2025 00:27:32 GMT  
		Size: 361.8 MB (361826517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a03b7dcf8eb9a3d0eae17f0c300ee315cbab8df4d7d7f82c44866c90bede0d1`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95136b3fae821b8ff1cda0a83742f9b0368d1dabffe1cb49ae4500ef73bc5d11`  
		Last Modified: Mon, 17 Nov 2025 23:27:48 GMT  
		Size: 16.5 MB (16460499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c216808eb9b5619482245cdde30a51c26dcb5debb8ca56839744fb0b941f2c`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 5.2 KB (5229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4d081d8d75d37fde8be605cb3c3c1fb168747b218eacc02941322e54b60ff9`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73d85ef3e7cb129366cdb8df2c50f17784ded11e6a086152bc3708411f790d`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b46a7a55f0a67e268360e502c33ca7ca3f21822c7b961fd1cf4f2502d8d5c1`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 4.7 KB (4740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a632a9cf387cffd82cc5147ddb56ad979ddb3a737cdc313dcca5b18aca7d0e9f`  
		Last Modified: Mon, 17 Nov 2025 23:27:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fdc72d8bdbb30aa24d23592db7110e76af486e7e4fee5494ec34c3baddeb8d`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21161a44ca4c28a6da78fa77bc91dba662ffa9b790995b585481f23482ff499`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a438517f2db73434265a7e1c98d6f136d441352208918b40475d5627b4396eca`  
		Last Modified: Mon, 17 Nov 2025 23:27:47 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:c9acd4ffe17250ffde29e644d5bf71f3969b41a46e3157162951993ce9b0fa4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5698759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec5e17532da79b22fa46a0197ad5361c07fce66ff304522e64852aa3b0e6f19`

```dockerfile
```

-	Layers:
	-	`sha256:7a3a123fc43c440d54a30eeb929de180651f04883a944fb3927d99def29f9c9a`  
		Last Modified: Tue, 18 Nov 2025 00:11:28 GMT  
		Size: 5.7 MB (5655533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c001dc05b47b0e77bd26d4faa7e3e5ffe3e96aa1c3f83c6a73371319469a3c3e`  
		Last Modified: Tue, 18 Nov 2025 00:11:29 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d167a7b5fc415aa6f80e45573bdd45cb5072fecfb6a3c71be50cdc4995c1e933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449100735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab32c5dfe3128b3350e8a84727e67ce8f148a93c87c75e229c093ddeb6dfb5`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:55:56 GMT
ENV container oci
# Mon, 17 Nov 2025 06:55:57 GMT
COPY dir:87932faf9829020ce186f9ca70767f10cf2708680f90badc643a8b214cc3a6f7 in /      
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:55:57 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:55:41Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:18:21 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 17 Nov 2025 23:18:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:25:29 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 17 Nov 2025 23:25:30 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:25:30 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 17 Nov 2025 23:25:30 GMT
RUN fc-cache -v # buildkit
# Mon, 17 Nov 2025 23:25:30 GMT
WORKDIR /usr/share/kibana
# Mon, 17 Nov 2025 23:25:30 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 17 Nov 2025 23:25:30 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:25:30 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:25:30 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 17 Nov 2025 23:25:30 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:25:31 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 17 Nov 2025 23:25:32 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 17 Nov 2025 23:25:32 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 17 Nov 2025 23:25:32 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Mon, 17 Nov 2025 23:25:32 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 17 Nov 2025 23:25:32 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:25:32 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 17 Nov 2025 23:25:32 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 17 Nov 2025 23:25:32 GMT
USER 1000
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624206ba177c95bb666893951daa1c025857dd33c7f41205fd4aa6f79dac381a`  
		Last Modified: Mon, 17 Nov 2025 23:26:50 GMT  
		Size: 19.5 MB (19499247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5715219322ddde8ea143a4dcd43eeaeb82c84ea37a28e7bdfd1b845d6f287e63`  
		Last Modified: Tue, 18 Nov 2025 08:33:13 GMT  
		Size: 374.8 MB (374844480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89b1569769d2aa91f1b2d79f569e2bb6605b9cb2af81a031bec310484c2b2a`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f64d9c55efdd0f77f32be3174ce1089ba76af395301343fdfbd9e51564fde95`  
		Last Modified: Mon, 17 Nov 2025 23:26:50 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555312ec979021eba794f732cefe55e59a767d8e6a60a313945369ba9a0f4c46`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1526874ccf2e4816f5484baec0735a2a8d84c1a045488acdba47cfa439bc9dd0`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bdad0c049d505f373750749204101da9f73808db45cf12b51f4c7968c2279a`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed00e5401b3cddcdfd42e493be16093469452cf8dfbf1c92b1cc444db8e7890`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 4.7 KB (4743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb1e8c6b0c147e1e4a9ddc771ab08a89572920be53614f602093e58d7af2291`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3073999a229b7da818d9826a0953b45baa94f342878bca1c5eccf558a644f389`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b194af3f200962962748e2484ec41240ed78d8748965ce73e4f01b8933c0d42c`  
		Last Modified: Mon, 17 Nov 2025 23:26:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9f0d4155c2a3215192d143e74c15aac4449fd02853b82dbe3f9d56f03e9`  
		Last Modified: Mon, 17 Nov 2025 23:26:50 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:9065bf99b271c45cdc86ac9e18cfc972e89bcfc7123adcc2aa98263fc9f31d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5697692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458fbdddceba0aa3e78d97cbae1f8a6a3f7bd1c0281d96070bafa34f7ab04e5e`

```dockerfile
```

-	Layers:
	-	`sha256:099b544670b5422a5c375bd93eb9e3ded113fbeabb087ca20618eb69fe18d3b8`  
		Last Modified: Tue, 18 Nov 2025 00:11:34 GMT  
		Size: 5.7 MB (5654209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ff3d21aa9b77d7f759de42286263d0acd144678b42e49afda00b15da5dbf7d`  
		Last Modified: Tue, 18 Nov 2025 00:11:35 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.1`

```console
$ docker pull kibana@sha256:245fd12e6c8d1b37b3ef23c504bd273e7d09b4f381359c3cb7dc28a8166be10e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.1` - linux; amd64

```console
$ docker pull kibana@sha256:86ac7e129901a9b27368562ce592834142659c5a4eadf579c7797ba8fed89433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.3 MB (436271707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c2b7ed00c745af041257136c355d388427609dc6ec705a709b0e6009c678cc`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:51:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:51:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:51:18 GMT
ENV container oci
# Mon, 17 Nov 2025 06:51:19 GMT
COPY dir:7cf80e1c5cade8bdab1a4d70632d27e8826f968a3bd11979550b2850547e929b in /      
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:51:19 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:51:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
COPY file:fde1a325755d265b4b09b708d833ef4334fd28d3649fcb5f69929257ca8b0d53 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:51:20 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:51:01Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:18:14 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 17 Nov 2025 23:18:14 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:27:06 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 17 Nov 2025 23:27:06 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:27:06 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 17 Nov 2025 23:27:07 GMT
RUN fc-cache -v # buildkit
# Mon, 17 Nov 2025 23:27:07 GMT
WORKDIR /usr/share/kibana
# Mon, 17 Nov 2025 23:27:07 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 17 Nov 2025 23:27:07 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:27:07 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:27:07 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 17 Nov 2025 23:27:07 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:27:07 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 17 Nov 2025 23:27:08 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 17 Nov 2025 23:27:08 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 17 Nov 2025 23:27:08 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Mon, 17 Nov 2025 23:27:08 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 17 Nov 2025 23:27:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:27:08 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 17 Nov 2025 23:27:08 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 17 Nov 2025 23:27:08 GMT
USER 1000
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c0abe34d06df07d1c061fd722ac493c4bc703954f55ea4b475ea2b5518bc71`  
		Last Modified: Mon, 17 Nov 2025 23:28:21 GMT  
		Size: 19.5 MB (19537014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d48d1227830453d7c5913a8f5fb658761acc34f9cad75eeb4d1e26d46d294`  
		Last Modified: Tue, 18 Nov 2025 00:11:53 GMT  
		Size: 360.2 MB (360196842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7bfe3dca9cd8b4d96804994e9241d5059e073d1e92e65837145eefd70853c`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd3eefdfbf7fcf85a8ebf955e9042477c4ea298043e3aea370736a10125b035`  
		Last Modified: Mon, 17 Nov 2025 23:28:21 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d60f653eb56ae8add76c87788fef638042a407dffdecc6a68de81c3341c35a6`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7ad413af728a05a45859e2ac1e64d349f128a515bd962adac076524ea4d8`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ee9671a22dc6c6b50a1bea897ae8f9d013dbb262d92b881bd64f5db653073`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2b1ba11be86f7ea5db497787c7abdfeb4edbe3543731ab570c1e720ec8727`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8d42b998d25f628585803d391f8af8f81c07640b23899b43c754da38c32261`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce800c3ac2bf409c1c0f253843bed277f8ad2708a92d3439d4394269220bc31b`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2d5aecc7d568bcc4a14bb7366bbd6895591f236ad71c2aaa1b81e1ba5b5aae`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acd075ae4ac686db050f641dc79219dd2cd5e6e1f2a6b2b00d64f7662f7a7f6`  
		Last Modified: Mon, 17 Nov 2025 23:28:19 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:e1ec88d7a2732fdec3b0554b22cdfbd5a18e26a5e3596392ecc121c989d2efae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8989d3e1b1538c455248cadb7ca61be3e32eeb7203133775c851f4c7cb59333c`

```dockerfile
```

-	Layers:
	-	`sha256:4dc5369ecdf071aa85e53c9702a5d0a357f6b6a9a3f873409fe0266544853ad0`  
		Last Modified: Tue, 18 Nov 2025 00:11:40 GMT  
		Size: 5.7 MB (5713256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d16acc879e4610009b621d0b71fdbe763730dc8075322a11118c63e57e89973`  
		Last Modified: Tue, 18 Nov 2025 00:11:41 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:7d3bc0267afe8861983ad180682e150831762af455096ff0ef4a3c9ad732b4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447486235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e38c4a12b7a910e3b75e7d9e150dea622767e79b5fe4e04724c360df1ea4500`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:55:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:55:56 GMT
ENV container oci
# Mon, 17 Nov 2025 06:55:57 GMT
COPY dir:87932faf9829020ce186f9ca70767f10cf2708680f90badc643a8b214cc3a6f7 in /      
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:55:57 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:55:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
COPY file:9de94f07a9e32b6295a1e34d66c814b476f5c78f9e3d5d56a9c5024309f451a8 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:55:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:55:41Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:18:31 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 17 Nov 2025 23:18:31 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:25:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 17 Nov 2025 23:25:48 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 17 Nov 2025 23:25:48 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 17 Nov 2025 23:25:48 GMT
RUN fc-cache -v # buildkit
# Mon, 17 Nov 2025 23:25:48 GMT
WORKDIR /usr/share/kibana
# Mon, 17 Nov 2025 23:25:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 17 Nov 2025 23:25:49 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 17 Nov 2025 23:25:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:25:49 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 17 Nov 2025 23:25:49 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:25:49 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 17 Nov 2025 23:25:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 17 Nov 2025 23:25:50 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 17 Nov 2025 23:25:50 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Mon, 17 Nov 2025 23:25:50 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 17 Nov 2025 23:25:51 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 17 Nov 2025 23:25:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 17 Nov 2025 23:25:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 17 Nov 2025 23:25:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:3c0c9428a7f3bd24ecc53d01a84f8e5daf4cde2806733046039c236a5821dc20`  
		Last Modified: Mon, 17 Nov 2025 07:42:16 GMT  
		Size: 38.2 MB (38200298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c03c202e4e9d2f004d408caf11871361d72cd120742462179bc563dd98c057`  
		Last Modified: Mon, 17 Nov 2025 23:27:12 GMT  
		Size: 19.5 MB (19499313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a86cfd74be4863659b1f7ece4c2e1c92fc172fa03b5cb3679ad116198c3d9b8`  
		Last Modified: Tue, 18 Nov 2025 01:33:01 GMT  
		Size: 373.2 MB (373229775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67e72f662c4536d374adf2274064bec96ccbc540470636e5cffcd8c8789662a`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3219f0bcc2594c02944499cf6d81940ea8be58ade61c6eeed16d52934629676f`  
		Last Modified: Mon, 17 Nov 2025 23:27:21 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02632925812f2d47f64786f64bc72dfaff1cf6554a2dc16be10b83715ffe7470`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069dac116ed1c635621e7f44c28c1a79fa045af23a9233e0f9cba2e8421243f`  
		Last Modified: Mon, 17 Nov 2025 23:27:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1403470379d7c453e0d017e55f6277d6064b822b63d26b02a641a94a791807f`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e43bb50d6ab6ac1ec1b3b34e640229f8580f81a2fc5f50c2e3511092a6a94b`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f54f6980344f5f2b846e66627312b6cc3fc8103b7d19c41f16bbc05cf4570`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6def0187b217de6e698c8d83bcd0ab4670a52dbe551d3b3497dd19f90c671440`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc221504d2c1aeadfdd20481bd92751cc717308bfad72b00ea35be4e154d0cf`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbf3a2e22aa182fbc46305460a9cb51d681a63ebe17cdda9d57a559962d4ebd`  
		Last Modified: Mon, 17 Nov 2025 23:27:10 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:1d33961b580ee718432c1318450ced24f26dfb328a0bf4f2091adb1b8d218e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1759af24fe847f865ea65ba2a5d8a9b9a6192659f8ff65f84f82f153b01d82d`

```dockerfile
```

-	Layers:
	-	`sha256:4db52b9f8239c853b324d2cce9e33d88346d28e16f4dac44b61a79f32f5b6998`  
		Last Modified: Tue, 18 Nov 2025 00:11:47 GMT  
		Size: 5.7 MB (5711932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa86123d24e2ca527df4ccb658d206dee8fefb8e8ba8b88a5594c8e20d37ca4`  
		Last Modified: Tue, 18 Nov 2025 00:11:48 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
