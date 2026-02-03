## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:67d597f82c400b13c0cfd3f134c78e3530c0bc216834551c5febd0975380b826
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:11c0a298d5ef1205cf2ec3ea32c52dd86382805eb599ded7e8633df03cfab185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12785926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4828abaf60df71f71de40643d5589a58846860ddf30c24f521b63980b9ced614`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:55 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:15:55 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 28 Jan 2026 02:15:55 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 28 Jan 2026 02:19:14 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:19:14 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:19:14 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:19:14 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:19:14 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:19:14 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:19:14 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:19:14 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:19:14 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:19:14 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:19:14 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:14 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e039def8eb7e6142c52b5d56bd7db8c89b4e1ad23571c7510d34c76deb93704`  
		Last Modified: Wed, 28 Jan 2026 02:19:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cacc13964d6975089b071cbf3cb6640097201cfa52f4e9a1f84c0d6f592503`  
		Last Modified: Wed, 28 Jan 2026 02:19:20 GMT  
		Size: 1.1 MB (1116690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841f81b1478901671b8d1e4d87aefb6ad6412b1a1333c0caa83012ecf25796b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:20 GMT  
		Size: 8.0 MB (8021415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aec9435a53e3578b338d7d0969bade1eb62145cb02a7e3f6b0d47162f62ca3d`  
		Last Modified: Wed, 28 Jan 2026 02:19:20 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8ab4f35c2586ea1c10c9bb42e52ff1ec59f0633e3f7c7fe1d3a04aa78ae05d`  
		Last Modified: Wed, 28 Jan 2026 02:19:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:a02ed2fd428fbd866864ea7e2efe2495240f1b2d271ebfea9b462cb5a7c19d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 KB (159908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73a082d0d7e15efd3547e38cda36b9b51eb1f33d27c93a7ef8d3c0e8cebcd71`

```dockerfile
```

-	Layers:
	-	`sha256:f298cbef1f561d71dcd79a19ad709b166cd5aff3386962b86bd38d2390893b0d`  
		Last Modified: Wed, 28 Jan 2026 02:19:20 GMT  
		Size: 142.9 KB (142860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff08cb3d5c07426cc3156abc89f0300062266e8dbff34d3421931b385374b762`  
		Last Modified: Wed, 28 Jan 2026 02:19:20 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:47d8c408984edee13e9f16cb2d54873ac7b976125f30b64f7384d3307a26f067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12336595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd14656d14331ded9911d87253ae90c70f285e990fa27ca6bca0217083d9dfb`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:00 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:20:00 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:20:01 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:20:01 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 28 Jan 2026 02:20:01 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 28 Jan 2026 02:24:51 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:24:51 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:24:51 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:24:51 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:24:51 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:24:51 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:24:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:24:51 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:24:51 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:24:51 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:24:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2a68e34e078099e94134d24feddbed5b8f32557051f3f938caf41e11c952e`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fdab165210050821af2a5f001d5baf8ccca79e3a009422af17370dad47f252`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 1.1 MB (1129836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49ba6c5c6be60d596e52593d7a1d3123519d7970a33420befa556d889a3bc3`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 7.8 MB (7836805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f145ec6b46d009f299a3286ae36570980ce83ff55f2000fa9dee92b3104bc317`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69d4b95bdade791673c1eeb6a6818cc455be2a0908d20fb81c621a81741a9f`  
		Last Modified: Wed, 28 Jan 2026 02:24:56 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:19fb84bb3687c06f77111bec63322ab97d7283d337714772d4f96948d6565afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 KB (16915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2537fb097272264eb4f8068e3096aaaea243f9c60592ca6272e8e6ab3d5397`

```dockerfile
```

-	Layers:
	-	`sha256:8ad8d8683e2f25ab6f97dd7ecfe2ea1c0dbebf39b215b06c30f62a78a9f3c19a`  
		Last Modified: Wed, 28 Jan 2026 02:24:55 GMT  
		Size: 16.9 KB (16915 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:8381867690c8f9a851d6d04f642df04c523173dc7b2d09c366819b22ad14f8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13234241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0927a23c3ffb78b855b6614e79cbb478e2d687d8e4ddd281503f3868f38c0be3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:33 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:33 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 28 Jan 2026 02:15:34 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 28 Jan 2026 02:19:49 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:19:49 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:19:49 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:19:49 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:19:49 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:19:49 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:19:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:19:49 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:19:49 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:19:49 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:19:49 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:49 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5d326835b03441f2d0547500e8b5b6656690da7a2ff55861d5c264ea343a83`  
		Last Modified: Wed, 28 Jan 2026 02:19:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7010c1534bbac2ca5df72008697b9f66e66597a1ca99133ea66928f8e813af30`  
		Last Modified: Wed, 28 Jan 2026 02:19:56 GMT  
		Size: 1.2 MB (1171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0f3569257823b47daa88a726588fc8036e267fb562f3398b1c33874ced31e3`  
		Last Modified: Wed, 28 Jan 2026 02:19:56 GMT  
		Size: 8.1 MB (8066291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d36b3217393e5d6208ba667e95e80c41e490ecca6d0d42312c37a1d83159ad8`  
		Last Modified: Wed, 28 Jan 2026 02:19:56 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57125704996435c761c26848340fc8180aa49a3375f1ddc3440e216c6ea62505`  
		Last Modified: Wed, 28 Jan 2026 02:19:56 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:ded820e13d9814b416f7903a27105df0c859d51dcb7dd5ab44411bbd2b489b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 KB (160025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b08edd1506473eb6118b8a07c1b3e6fe96d553a8ca36b2cfa4aec5820514968`

```dockerfile
```

-	Layers:
	-	`sha256:b38c81a463b11d91af7b34bcacd0e3ac42a05c09b395d227e6fcd90e65ee5f97`  
		Last Modified: Wed, 28 Jan 2026 02:19:55 GMT  
		Size: 142.9 KB (142880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15de479200558222c18ed2410b3f98b6fa9d9d7481d5793cadaad84c5e311c1`  
		Last Modified: Wed, 28 Jan 2026 02:19:55 GMT  
		Size: 17.1 KB (17145 bytes)  
		MIME: application/vnd.in-toto+json
