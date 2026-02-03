<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10`](#eggdrop110)
-	[`eggdrop:1.10.0`](#eggdrop1100)
-	[`eggdrop:1.10.1rc1`](#eggdrop1101rc1)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10`

```console
$ docker pull eggdrop@sha256:d2aa90ef6eae54927d74b22b0dd43da97eda6b188654e1475f00e78fd4629062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10` - linux; amd64

```console
$ docker pull eggdrop@sha256:75604f971a95fc3315b618630920ed7b16ad0bad4e32423780835c1a935a392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17470125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484fb7a359f5cd0eb36db932e8d7f9182ab4da24806051e57c4f620ac46b14cf`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:56 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:39 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:39 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:39 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:39 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b447b85aab30cbd4e93becaad9e1208b0a764b53c40aef3dfe59eb276d774865`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b578563d5af8bbbd476ae5c994768e549362f58ca6a42f53e6440b2ae6c51ad`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 MB (1115911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114e6e6716e78dd8ac2824cf6a70806321dff723fffd1656200948827841b75`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 12.7 MB (12722284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697ebd10c79fa694752b817a0ead2f05dd1ec5caee6852a4bdaa8f9e747e00d1`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e27ee35abd6ced910bc0bdcc35503e055d42386a5bb1f31c7e240238603af7`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3d366e9f3a29c9637105b4ff5da62b54f062494788ce8ad4735e44976af31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 KB (159261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3a7312cd85c5d86bcf78a88b83a605d2398a6835dc69268e4c9a5f167aea1d`

```dockerfile
```

-	Layers:
	-	`sha256:0fca8dee8c5827f93ecc12b6f7d0d95290c0e133f5296c03e4639a7de5582959`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.5 KB (140534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23404d87d4058c8ee642ae3af674a727b34422f5928d2b394f9a879c069c8df3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f726d373a0f0afefd537a549e887de61ca5ebe2d551ccc93c1773d5b18db1e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17077691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806430cc198130a29da24e437b36157b82dd4dfc6587ce62864358a32f59f937`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.20.9-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:20:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:20:18 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:23:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:23:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:23:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:23:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:23:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:23:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c84155fcd6ec1b5c6b681a4d3a533e0b8ba16d59b99ea51039e0b0675632930c`  
		Last Modified: Wed, 28 Jan 2026 01:18:44 GMT  
		Size: 3.4 MB (3372363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14775d4c0b0bb919c92ea87d4c52ce33a1b75f672736f9eefc88ecc7d7338866`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d010ebe6b6f9277c0e3ae2f9b97ad0839cbac412a84f2a3bd82081942911d`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 1.1 MB (1130429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21fadba41c8bc3e4beb2d798e558fb811d1ef49932d32cd3511bb4fc64e209`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 12.6 MB (12570823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbe2c20ead58a09a465d301aaebcaf32cc491219a51ff6aa3b7515c128b461`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991196029883daff61803b48f72e3d935122040b40ea654df270ed93b93c6dc`  
		Last Modified: Wed, 28 Jan 2026 02:23:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:e68fdf291048bd59b5a914e6ac94b91871223343b5854be971fe265c337eff8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fce92b34f08cccf7250b939cbb0ebb1604d438495eae52381875216222fd2`

```dockerfile
```

-	Layers:
	-	`sha256:c586be384a060ce9a85733bc430c6d2c9a8043c15e55d9c3977e3a1af4bef659`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 18.6 KB (18619 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:38cf62d26331fd049ca2f5d5b3019cf0e01276ff8b924d2ff848652214fb15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecb88b3c8f94581811f88893f650787301460f320a0029e84d2adfd9575313`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:34 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:34 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:38 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:38 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:38 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:38 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19a964560edb0c0f83f231cc87e7375585adcaac10463b06bbdc93ed314fc7`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec72b194072ac61d9d30264898bae7ca9508d13766fa4228956f974885de617`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.2 MB (1211877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bcdaddba9569dddc649c66079b31b6dbf3e6c25bba18a9e9b77a4836b46a9a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 12.9 MB (12857520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a7c818db83516965e8cb1105908c2931829f0d2cb6bddfa294d6c151c6e5a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430dc418511aaa4f733285115389bdb5cb0aff5941295ea7d11a1d3d415f50da`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8434220176204ec11de29cc19482ccfab749781a4547957352170e7729b67e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 KB (159452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e6d47e09077cff93d54cd320b9ad09c71530d36298b6acad1bebef65166527`

```dockerfile
```

-	Layers:
	-	`sha256:fa324f4563bba4f1b5e8bf6dfac63e2c19b3d54e389c94ac161f7de7e6bc5944`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.6 KB (140590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe221b196f9139c99e479c14b73b286f065f2f9ab7233d397462f48bcba7b1b3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.9 KB (18862 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.0`

```console
$ docker pull eggdrop@sha256:d2aa90ef6eae54927d74b22b0dd43da97eda6b188654e1475f00e78fd4629062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.0` - linux; amd64

```console
$ docker pull eggdrop@sha256:75604f971a95fc3315b618630920ed7b16ad0bad4e32423780835c1a935a392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17470125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484fb7a359f5cd0eb36db932e8d7f9182ab4da24806051e57c4f620ac46b14cf`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:56 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:39 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:39 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:39 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:39 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b447b85aab30cbd4e93becaad9e1208b0a764b53c40aef3dfe59eb276d774865`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b578563d5af8bbbd476ae5c994768e549362f58ca6a42f53e6440b2ae6c51ad`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 MB (1115911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114e6e6716e78dd8ac2824cf6a70806321dff723fffd1656200948827841b75`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 12.7 MB (12722284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697ebd10c79fa694752b817a0ead2f05dd1ec5caee6852a4bdaa8f9e747e00d1`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e27ee35abd6ced910bc0bdcc35503e055d42386a5bb1f31c7e240238603af7`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3d366e9f3a29c9637105b4ff5da62b54f062494788ce8ad4735e44976af31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 KB (159261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3a7312cd85c5d86bcf78a88b83a605d2398a6835dc69268e4c9a5f167aea1d`

```dockerfile
```

-	Layers:
	-	`sha256:0fca8dee8c5827f93ecc12b6f7d0d95290c0e133f5296c03e4639a7de5582959`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.5 KB (140534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23404d87d4058c8ee642ae3af674a727b34422f5928d2b394f9a879c069c8df3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f726d373a0f0afefd537a549e887de61ca5ebe2d551ccc93c1773d5b18db1e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17077691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806430cc198130a29da24e437b36157b82dd4dfc6587ce62864358a32f59f937`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.20.9-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:20:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:20:18 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:23:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:23:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:23:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:23:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:23:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:23:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c84155fcd6ec1b5c6b681a4d3a533e0b8ba16d59b99ea51039e0b0675632930c`  
		Last Modified: Wed, 28 Jan 2026 01:18:44 GMT  
		Size: 3.4 MB (3372363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14775d4c0b0bb919c92ea87d4c52ce33a1b75f672736f9eefc88ecc7d7338866`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d010ebe6b6f9277c0e3ae2f9b97ad0839cbac412a84f2a3bd82081942911d`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 1.1 MB (1130429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21fadba41c8bc3e4beb2d798e558fb811d1ef49932d32cd3511bb4fc64e209`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 12.6 MB (12570823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbe2c20ead58a09a465d301aaebcaf32cc491219a51ff6aa3b7515c128b461`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991196029883daff61803b48f72e3d935122040b40ea654df270ed93b93c6dc`  
		Last Modified: Wed, 28 Jan 2026 02:23:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:e68fdf291048bd59b5a914e6ac94b91871223343b5854be971fe265c337eff8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fce92b34f08cccf7250b939cbb0ebb1604d438495eae52381875216222fd2`

```dockerfile
```

-	Layers:
	-	`sha256:c586be384a060ce9a85733bc430c6d2c9a8043c15e55d9c3977e3a1af4bef659`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 18.6 KB (18619 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:38cf62d26331fd049ca2f5d5b3019cf0e01276ff8b924d2ff848652214fb15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecb88b3c8f94581811f88893f650787301460f320a0029e84d2adfd9575313`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:34 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:34 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:38 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:38 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:38 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:38 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19a964560edb0c0f83f231cc87e7375585adcaac10463b06bbdc93ed314fc7`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec72b194072ac61d9d30264898bae7ca9508d13766fa4228956f974885de617`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.2 MB (1211877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bcdaddba9569dddc649c66079b31b6dbf3e6c25bba18a9e9b77a4836b46a9a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 12.9 MB (12857520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a7c818db83516965e8cb1105908c2931829f0d2cb6bddfa294d6c151c6e5a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430dc418511aaa4f733285115389bdb5cb0aff5941295ea7d11a1d3d415f50da`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8434220176204ec11de29cc19482ccfab749781a4547957352170e7729b67e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 KB (159452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e6d47e09077cff93d54cd320b9ad09c71530d36298b6acad1bebef65166527`

```dockerfile
```

-	Layers:
	-	`sha256:fa324f4563bba4f1b5e8bf6dfac63e2c19b3d54e389c94ac161f7de7e6bc5944`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.6 KB (140590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe221b196f9139c99e479c14b73b286f065f2f9ab7233d397462f48bcba7b1b3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.9 KB (18862 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.1rc1`

```console
$ docker pull eggdrop@sha256:b3a2d4771e8f1c5e0a895263986a2360bc24565bc1f6df227339a05d3dbca3c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.1rc1` - linux; amd64

```console
$ docker pull eggdrop@sha256:61bed9c2ebb580500409d97369083a1e82299369c433875f877a6bc9b9be0ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12776128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4c9d9fb4908c181663faa52f040e7623a8d6186ab69c253d2886007179c801`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:57 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:57 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:58 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:20:13 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1rc1.tar.gz.asc eggdrop-1.10.1rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.1rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1rc1.tar.gz   && rm eggdrop-1.10.1rc1.tar.gz   && ( cd eggdrop-1.10.1rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:20:13 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:20:13 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:20:13 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:20:13 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:20:13 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:20:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:20:13 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:20:13 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:20:13 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:20:13 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:13 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fcbe5ae451c702e909a2713a85294487e0e1e0f0372f6465f92b9441a48035`  
		Last Modified: Wed, 28 Jan 2026 02:20:19 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14952b7bd30dae5f5ad75babbb05dbe612ea9f8282ce909e37793173eb2171d`  
		Last Modified: Wed, 28 Jan 2026 02:20:19 GMT  
		Size: 1.1 MB (1116700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bca41d88acce03c8348a396d27737a0df7e71288d855bf031e1e18f10d9f4e`  
		Last Modified: Wed, 28 Jan 2026 02:20:19 GMT  
		Size: 8.0 MB (8011614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82246678008f4599a3a53df80062262b9f434581723f51d72b60e58ff1500f11`  
		Last Modified: Wed, 28 Jan 2026 02:20:19 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff6f2443cf663046832fd06e1024a5b35dc6f880a4ab3453bcf04024002164d`  
		Last Modified: Wed, 28 Jan 2026 02:20:20 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:44d655b7b8211c99fb152c1be27a5d6a3a370058e1494d0b690fbb29c675cf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 KB (160525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5d76dfe3ca3c8935deebacf9626d481af5fad2089e1d5f86a6a9bac7720be1`

```dockerfile
```

-	Layers:
	-	`sha256:0142b798887139f78f64d1bced95aa8f59b959f1e49762757168f063424ba5a6`  
		Last Modified: Wed, 28 Jan 2026 02:20:19 GMT  
		Size: 142.9 KB (142864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:678707dac618e8e418a353c81adb0784e32cb01125fef86482203c70cd953cf2`  
		Last Modified: Wed, 28 Jan 2026 02:20:19 GMT  
		Size: 17.7 KB (17661 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:3f54e1c8e9536fcc3d3b6963101f59d125b2eb7846ed609ddb0eeb3ebb9c4dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12328647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c07b9323ab3cbd75e9b23eb69f9bd3215cf8e54abcae74281ea5af00d04a79`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:40 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:20:40 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:20:41 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:25:36 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1rc1.tar.gz.asc eggdrop-1.10.1rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.1rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1rc1.tar.gz   && rm eggdrop-1.10.1rc1.tar.gz   && ( cd eggdrop-1.10.1rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:25:36 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:25:36 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:25:36 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:25:36 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:25:36 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:25:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:25:36 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:25:36 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:25:36 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:25:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7759b10deffee89b81253c5cf1d7cd0996ea8821b1d1693f2c386b89715e55aa`  
		Last Modified: Wed, 28 Jan 2026 02:25:40 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f708b80e6b6360b791df4e05544fc9c7df6a1d5ef0502df6956ec49d88ef9c`  
		Last Modified: Wed, 28 Jan 2026 02:25:41 GMT  
		Size: 1.1 MB (1129835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9022cc9789162d800d915fe8155f5af31c734d264832f5ccd46abb02dc2099f7`  
		Last Modified: Wed, 28 Jan 2026 02:25:41 GMT  
		Size: 7.8 MB (7828869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f352ea9a6a24e6374d35c49e351ff859da30e789efc977ac7bddc329004cca`  
		Last Modified: Wed, 28 Jan 2026 02:25:41 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dda47a14f4f66ee5f0537a5864b5c0583a923dd078882f110d581ab2bafc9`  
		Last Modified: Wed, 28 Jan 2026 02:25:42 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:e347a3a1b0895bc20817882e12bc12d02b5267b4e59d1e8dc7d91acf5561704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78bc78cf190ccfc0aff91ebed292e4fd38f499a82a74047cc7b5626f641997f`

```dockerfile
```

-	Layers:
	-	`sha256:10097d82d53a2404ae48168d6df02a3f6bd0a06c167fad868d2af53a9b7ead53`  
		Last Modified: Wed, 28 Jan 2026 02:25:41 GMT  
		Size: 17.5 KB (17528 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1rc1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:f0de7ad2c18b695fb357fd53408acf0a60a5e2c03563409c1f7bf3e4637dbb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13224606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1126597d211b70a0d9926dcda6a84c626a9c71445b71b4a7285de9657475a562`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:58 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:58 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:58 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:20:30 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1rc1.tar.gz.asc eggdrop-1.10.1rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.1rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1rc1.tar.gz   && rm eggdrop-1.10.1rc1.tar.gz   && ( cd eggdrop-1.10.1rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:20:30 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:20:30 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:20:30 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:20:30 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:20:30 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:20:30 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:20:30 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:20:30 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:20:30 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:20:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdeb8276d157bc566465d612c28e033b6890f3e397688b89a1817fd47b78b1a`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d135a4405b01f9b3ff6733ee1d4c782014a5721f4017621c36559cc8c4f2aa`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 1.2 MB (1171007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2871df6caf1bd006d7d3d42278e71d21f337542278fc1e2f78aeb5ed846cd9e0`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 8.1 MB (8056646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0081be326a139628707fac4ba54edb421e4c7b1804e7c9feb0216285a7e0e022`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de30061866b556e93880717a4e77777a3ba7a9b3673d1cbe852fb0efbac0e9a`  
		Last Modified: Wed, 28 Jan 2026 02:20:37 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f233077c2815ce3fe9b4e657b208f57eb48e2847f6629e0cf7f4de7319aa8c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 KB (160643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02185412084a280f75c56bd1c4dd3df5847b87c7944bc3feb405ffae5bdd08f1`

```dockerfile
```

-	Layers:
	-	`sha256:6cf890619af1eb0aee97f2f792ef6b0b56430a43ac2e14b9fbd6206bf1c199be`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 142.9 KB (142884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d2c209e85feb70ca3959b1b2cbc1ff99fa60b3d78837e09549fa5b611c56af7`  
		Last Modified: Wed, 28 Jan 2026 02:20:36 GMT  
		Size: 17.8 KB (17759 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:f0edf2cc118b6f8d51ca5ca457e7ed39de781a24ba45503307ca8979fab9c55d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:8345fb94c180353101406913a645677e5940f3849a8d1ec7a6c24a119f3ca19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12286759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d06ee77c5387301b5c11bdea42e73d95b1031dc3c7d8c04a578e1c242c9c411`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:03:48 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7316e998276c82f3bb2369be124ab05d22b859cc8d53ffb41fccd100ad00208c`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3603468f0553ffc9a30a31992b4e5f2ea5d2abe9306c652231127acb406f088`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7bf60cc91feff70af89ac01f4d4292da900b0e22441463a0ee5f8c6c00b24`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 2.9 MB (2889546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3823d763363aea3e9d7da677d8b24266f2e33edf41767c3b1a033635234ae5`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 6.0 MB (5962767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e6eb4b83c6aa67cb71e5b24b549bf3367ba4f61e864341240540a7102524ad`  
		Last Modified: Wed, 08 Oct 2025 22:36:13 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc219421bf835c287336bfa31297a448e45fb284e5798787c89bf438d69390`  
		Last Modified: Wed, 08 Oct 2025 22:36:13 GMT  
		Size: 698.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:33e473d1913ee8341924f97ebd0a17972c569e2e9550f4f3c353d0a1aae1e86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb9a48ea8a3403c9dcd0ab6b65a14b89226df76f1627c39ff03ff9c8df4368a`

```dockerfile
```

-	Layers:
	-	`sha256:de4082dfbcb694cf00e6f51b12123b36173ce73dfc084c73c27f9f9d5cc0bf95`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 1.0 MB (1046379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28220d2e07e771ee3aa0a818c21e600c6f0eadb32341fba513b4bac359f50dca`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d52aecd62ec221026a308c30a0e17a70489f99f1dd5efcbb013a3d6947c942bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11943622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3425d372ae25ab7e42c1698fdf61d991995def418bb6077885b6c182ab5a0e88`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.9-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:93e88a4aad08082395ce41ebaca8e4678e1148db5e8947e4c39599181a9ee4ba`  
		Last Modified: Wed, 08 Oct 2025 21:00:31 GMT  
		Size: 3.2 MB (3176528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba54712bd4e497e05eed04949efa0571b4d765e5e9782be6616ef929329f74d4`  
		Last Modified: Wed, 08 Oct 2025 21:35:04 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa8dd1697f1496ff8411d5030f4f18e27ff4afb16e6769790b66b59eb7075a0`  
		Last Modified: Wed, 08 Oct 2025 21:35:04 GMT  
		Size: 11.0 KB (10963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62159d7e2d9faddf7d2f6bb04e9b984003c3475a0d50a037d8b694ea3aaa2ea4`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 2.9 MB (2895011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fec9ebf9ea28d947baa0058a462a1625384dec6ae60b90cd009cebe8b03169`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 5.9 MB (5857312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3fa352f7674af716153a72dc300311be2dd3a14f48c2d95742068eaf19467`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53a3156f16914dfbbe09b9c9b876971edfebefe9490553e9ac555d3af1fc5fb`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 698.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f8c21fb942736141db6c7599af03921811dd4f2643904fb9565101db36bc4ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea33bf7860a69b82ea91aa1a2f2a7186e4d3cafab8be347dd58b00f31959db39`

```dockerfile
```

-	Layers:
	-	`sha256:4cc1a707e817359a179c629629333e4e8e7199b900db70d9ea9cfaba03f40248`  
		Last Modified: Wed, 08 Oct 2025 21:35:04 GMT  
		Size: 19.2 KB (19244 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7d7130df667ddbb9e80bbe34c2d1154cb535f3b3b864fe7b4fd34b7af07cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe13d5c10ee40d1b9d76bf823efb051baca0347bf56dc4b7b3799ccbf26f0df`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:03:49 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0763017031149ed15ce1ee44a7cd6fd75ffe716aadecf3daf96edf941682e8`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94e3a4663355b28eea39ba6acb6bb9f88150989683f154249a7342c5515877`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984d9f8b23b71220a762e17a55fb8411af119bf5d4b5c3a229d19584bd40396a`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 3.0 MB (3024121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74809264f5f9235c4d65c2ced5cc035840ae88bb37baf79102afe81f59336b53`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 6.0 MB (6013177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54a9598fe40e9ac1982ab0c88ca0ddd4732cda51704ac4eb65f7be824312108`  
		Last Modified: Wed, 08 Oct 2025 21:30:13 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6d7c3b34fb8ff14cd53ea3bfacb65776bc4976a77e3a256f6f0fe49a8ddf0b`  
		Last Modified: Wed, 08 Oct 2025 21:30:13 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f97f6dd1694c0a9e9e11c149bbd1ae5d010e8df5ec9577962c4156222e7cfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0070a073365f7458cac6f7cfad78d8624b70428ed2f3a1064a7d48c86865ffb8`

```dockerfile
```

-	Layers:
	-	`sha256:3b7a3e44cab5aa561ae5e32b40bb124d8971de3dc09ea896ae4369d00d3fad01`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 1.0 MB (1046411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcc60a7d4de67aca13e7ad33dcaf9ed8fe3ad050248d0b9a08f773ea1876f23`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:f0edf2cc118b6f8d51ca5ca457e7ed39de781a24ba45503307ca8979fab9c55d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:8345fb94c180353101406913a645677e5940f3849a8d1ec7a6c24a119f3ca19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12286759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d06ee77c5387301b5c11bdea42e73d95b1031dc3c7d8c04a578e1c242c9c411`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:03:48 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7316e998276c82f3bb2369be124ab05d22b859cc8d53ffb41fccd100ad00208c`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3603468f0553ffc9a30a31992b4e5f2ea5d2abe9306c652231127acb406f088`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b7bf60cc91feff70af89ac01f4d4292da900b0e22441463a0ee5f8c6c00b24`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 2.9 MB (2889546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3823d763363aea3e9d7da677d8b24266f2e33edf41767c3b1a033635234ae5`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 6.0 MB (5962767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e6eb4b83c6aa67cb71e5b24b549bf3367ba4f61e864341240540a7102524ad`  
		Last Modified: Wed, 08 Oct 2025 22:36:13 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc219421bf835c287336bfa31297a448e45fb284e5798787c89bf438d69390`  
		Last Modified: Wed, 08 Oct 2025 22:36:13 GMT  
		Size: 698.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:33e473d1913ee8341924f97ebd0a17972c569e2e9550f4f3c353d0a1aae1e86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb9a48ea8a3403c9dcd0ab6b65a14b89226df76f1627c39ff03ff9c8df4368a`

```dockerfile
```

-	Layers:
	-	`sha256:de4082dfbcb694cf00e6f51b12123b36173ce73dfc084c73c27f9f9d5cc0bf95`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 1.0 MB (1046379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28220d2e07e771ee3aa0a818c21e600c6f0eadb32341fba513b4bac359f50dca`  
		Last Modified: Wed, 08 Oct 2025 22:36:12 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d52aecd62ec221026a308c30a0e17a70489f99f1dd5efcbb013a3d6947c942bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11943622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3425d372ae25ab7e42c1698fdf61d991995def418bb6077885b6c182ab5a0e88`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.9-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:93e88a4aad08082395ce41ebaca8e4678e1148db5e8947e4c39599181a9ee4ba`  
		Last Modified: Wed, 08 Oct 2025 21:00:31 GMT  
		Size: 3.2 MB (3176528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba54712bd4e497e05eed04949efa0571b4d765e5e9782be6616ef929329f74d4`  
		Last Modified: Wed, 08 Oct 2025 21:35:04 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa8dd1697f1496ff8411d5030f4f18e27ff4afb16e6769790b66b59eb7075a0`  
		Last Modified: Wed, 08 Oct 2025 21:35:04 GMT  
		Size: 11.0 KB (10963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62159d7e2d9faddf7d2f6bb04e9b984003c3475a0d50a037d8b694ea3aaa2ea4`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 2.9 MB (2895011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fec9ebf9ea28d947baa0058a462a1625384dec6ae60b90cd009cebe8b03169`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 5.9 MB (5857312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3fa352f7674af716153a72dc300311be2dd3a14f48c2d95742068eaf19467`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53a3156f16914dfbbe09b9c9b876971edfebefe9490553e9ac555d3af1fc5fb`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 698.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f8c21fb942736141db6c7599af03921811dd4f2643904fb9565101db36bc4ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea33bf7860a69b82ea91aa1a2f2a7186e4d3cafab8be347dd58b00f31959db39`

```dockerfile
```

-	Layers:
	-	`sha256:4cc1a707e817359a179c629629333e4e8e7199b900db70d9ea9cfaba03f40248`  
		Last Modified: Wed, 08 Oct 2025 21:35:04 GMT  
		Size: 19.2 KB (19244 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7d7130df667ddbb9e80bbe34c2d1154cb535f3b3b864fe7b4fd34b7af07cd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe13d5c10ee40d1b9d76bf823efb051baca0347bf56dc4b7b3799ccbf26f0df`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:03:49 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0763017031149ed15ce1ee44a7cd6fd75ffe716aadecf3daf96edf941682e8`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94e3a4663355b28eea39ba6acb6bb9f88150989683f154249a7342c5515877`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984d9f8b23b71220a762e17a55fb8411af119bf5d4b5c3a229d19584bd40396a`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 3.0 MB (3024121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74809264f5f9235c4d65c2ced5cc035840ae88bb37baf79102afe81f59336b53`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 6.0 MB (6013177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54a9598fe40e9ac1982ab0c88ca0ddd4732cda51704ac4eb65f7be824312108`  
		Last Modified: Wed, 08 Oct 2025 21:30:13 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6d7c3b34fb8ff14cd53ea3bfacb65776bc4976a77e3a256f6f0fe49a8ddf0b`  
		Last Modified: Wed, 08 Oct 2025 21:30:13 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f97f6dd1694c0a9e9e11c149bbd1ae5d010e8df5ec9577962c4156222e7cfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0070a073365f7458cac6f7cfad78d8624b70428ed2f3a1064a7d48c86865ffb8`

```dockerfile
```

-	Layers:
	-	`sha256:3b7a3e44cab5aa561ae5e32b40bb124d8971de3dc09ea896ae4369d00d3fad01`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 1.0 MB (1046411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcc60a7d4de67aca13e7ad33dcaf9ed8fe3ad050248d0b9a08f773ea1876f23`  
		Last Modified: Wed, 08 Oct 2025 21:30:12 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

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

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:d2aa90ef6eae54927d74b22b0dd43da97eda6b188654e1475f00e78fd4629062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:75604f971a95fc3315b618630920ed7b16ad0bad4e32423780835c1a935a392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17470125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484fb7a359f5cd0eb36db932e8d7f9182ab4da24806051e57c4f620ac46b14cf`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:56 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:39 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:39 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:39 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:39 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b447b85aab30cbd4e93becaad9e1208b0a764b53c40aef3dfe59eb276d774865`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b578563d5af8bbbd476ae5c994768e549362f58ca6a42f53e6440b2ae6c51ad`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 MB (1115911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114e6e6716e78dd8ac2824cf6a70806321dff723fffd1656200948827841b75`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 12.7 MB (12722284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697ebd10c79fa694752b817a0ead2f05dd1ec5caee6852a4bdaa8f9e747e00d1`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e27ee35abd6ced910bc0bdcc35503e055d42386a5bb1f31c7e240238603af7`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3d366e9f3a29c9637105b4ff5da62b54f062494788ce8ad4735e44976af31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 KB (159261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3a7312cd85c5d86bcf78a88b83a605d2398a6835dc69268e4c9a5f167aea1d`

```dockerfile
```

-	Layers:
	-	`sha256:0fca8dee8c5827f93ecc12b6f7d0d95290c0e133f5296c03e4639a7de5582959`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.5 KB (140534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23404d87d4058c8ee642ae3af674a727b34422f5928d2b394f9a879c069c8df3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f726d373a0f0afefd537a549e887de61ca5ebe2d551ccc93c1773d5b18db1e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17077691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806430cc198130a29da24e437b36157b82dd4dfc6587ce62864358a32f59f937`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.20.9-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:20:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:20:18 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:23:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:23:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:23:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:23:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:23:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:23:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c84155fcd6ec1b5c6b681a4d3a533e0b8ba16d59b99ea51039e0b0675632930c`  
		Last Modified: Wed, 28 Jan 2026 01:18:44 GMT  
		Size: 3.4 MB (3372363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14775d4c0b0bb919c92ea87d4c52ce33a1b75f672736f9eefc88ecc7d7338866`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d010ebe6b6f9277c0e3ae2f9b97ad0839cbac412a84f2a3bd82081942911d`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 1.1 MB (1130429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21fadba41c8bc3e4beb2d798e558fb811d1ef49932d32cd3511bb4fc64e209`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 12.6 MB (12570823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbe2c20ead58a09a465d301aaebcaf32cc491219a51ff6aa3b7515c128b461`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991196029883daff61803b48f72e3d935122040b40ea654df270ed93b93c6dc`  
		Last Modified: Wed, 28 Jan 2026 02:23:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:e68fdf291048bd59b5a914e6ac94b91871223343b5854be971fe265c337eff8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fce92b34f08cccf7250b939cbb0ebb1604d438495eae52381875216222fd2`

```dockerfile
```

-	Layers:
	-	`sha256:c586be384a060ce9a85733bc430c6d2c9a8043c15e55d9c3977e3a1af4bef659`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 18.6 KB (18619 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:38cf62d26331fd049ca2f5d5b3019cf0e01276ff8b924d2ff848652214fb15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecb88b3c8f94581811f88893f650787301460f320a0029e84d2adfd9575313`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:34 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:34 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:38 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:38 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:38 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:38 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19a964560edb0c0f83f231cc87e7375585adcaac10463b06bbdc93ed314fc7`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec72b194072ac61d9d30264898bae7ca9508d13766fa4228956f974885de617`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.2 MB (1211877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bcdaddba9569dddc649c66079b31b6dbf3e6c25bba18a9e9b77a4836b46a9a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 12.9 MB (12857520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a7c818db83516965e8cb1105908c2931829f0d2cb6bddfa294d6c151c6e5a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430dc418511aaa4f733285115389bdb5cb0aff5941295ea7d11a1d3d415f50da`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8434220176204ec11de29cc19482ccfab749781a4547957352170e7729b67e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 KB (159452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e6d47e09077cff93d54cd320b9ad09c71530d36298b6acad1bebef65166527`

```dockerfile
```

-	Layers:
	-	`sha256:fa324f4563bba4f1b5e8bf6dfac63e2c19b3d54e389c94ac161f7de7e6bc5944`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.6 KB (140590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe221b196f9139c99e479c14b73b286f065f2f9ab7233d397462f48bcba7b1b3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.9 KB (18862 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:d2aa90ef6eae54927d74b22b0dd43da97eda6b188654e1475f00e78fd4629062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:75604f971a95fc3315b618630920ed7b16ad0bad4e32423780835c1a935a392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17470125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484fb7a359f5cd0eb36db932e8d7f9182ab4da24806051e57c4f620ac46b14cf`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:56 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:39 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:39 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:39 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:39 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b447b85aab30cbd4e93becaad9e1208b0a764b53c40aef3dfe59eb276d774865`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b578563d5af8bbbd476ae5c994768e549362f58ca6a42f53e6440b2ae6c51ad`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 MB (1115911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114e6e6716e78dd8ac2824cf6a70806321dff723fffd1656200948827841b75`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 12.7 MB (12722284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697ebd10c79fa694752b817a0ead2f05dd1ec5caee6852a4bdaa8f9e747e00d1`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e27ee35abd6ced910bc0bdcc35503e055d42386a5bb1f31c7e240238603af7`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3d366e9f3a29c9637105b4ff5da62b54f062494788ce8ad4735e44976af31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 KB (159261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3a7312cd85c5d86bcf78a88b83a605d2398a6835dc69268e4c9a5f167aea1d`

```dockerfile
```

-	Layers:
	-	`sha256:0fca8dee8c5827f93ecc12b6f7d0d95290c0e133f5296c03e4639a7de5582959`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.5 KB (140534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23404d87d4058c8ee642ae3af674a727b34422f5928d2b394f9a879c069c8df3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f726d373a0f0afefd537a549e887de61ca5ebe2d551ccc93c1773d5b18db1e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17077691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806430cc198130a29da24e437b36157b82dd4dfc6587ce62864358a32f59f937`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.20.9-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:20:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:20:18 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:23:28 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:23:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:23:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:23:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:23:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:23:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:23:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:23:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c84155fcd6ec1b5c6b681a4d3a533e0b8ba16d59b99ea51039e0b0675632930c`  
		Last Modified: Wed, 28 Jan 2026 01:18:44 GMT  
		Size: 3.4 MB (3372363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14775d4c0b0bb919c92ea87d4c52ce33a1b75f672736f9eefc88ecc7d7338866`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d010ebe6b6f9277c0e3ae2f9b97ad0839cbac412a84f2a3bd82081942911d`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 1.1 MB (1130429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21fadba41c8bc3e4beb2d798e558fb811d1ef49932d32cd3511bb4fc64e209`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 12.6 MB (12570823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbe2c20ead58a09a465d301aaebcaf32cc491219a51ff6aa3b7515c128b461`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991196029883daff61803b48f72e3d935122040b40ea654df270ed93b93c6dc`  
		Last Modified: Wed, 28 Jan 2026 02:23:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:e68fdf291048bd59b5a914e6ac94b91871223343b5854be971fe265c337eff8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fce92b34f08cccf7250b939cbb0ebb1604d438495eae52381875216222fd2`

```dockerfile
```

-	Layers:
	-	`sha256:c586be384a060ce9a85733bc430c6d2c9a8043c15e55d9c3977e3a1af4bef659`  
		Last Modified: Wed, 28 Jan 2026 02:23:33 GMT  
		Size: 18.6 KB (18619 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:38cf62d26331fd049ca2f5d5b3019cf0e01276ff8b924d2ff848652214fb15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecb88b3c8f94581811f88893f650787301460f320a0029e84d2adfd9575313`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:34 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:34 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:38 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:38 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:38 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:38 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19a964560edb0c0f83f231cc87e7375585adcaac10463b06bbdc93ed314fc7`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec72b194072ac61d9d30264898bae7ca9508d13766fa4228956f974885de617`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.2 MB (1211877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bcdaddba9569dddc649c66079b31b6dbf3e6c25bba18a9e9b77a4836b46a9a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 12.9 MB (12857520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a7c818db83516965e8cb1105908c2931829f0d2cb6bddfa294d6c151c6e5a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430dc418511aaa4f733285115389bdb5cb0aff5941295ea7d11a1d3d415f50da`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8434220176204ec11de29cc19482ccfab749781a4547957352170e7729b67e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 KB (159452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e6d47e09077cff93d54cd320b9ad09c71530d36298b6acad1bebef65166527`

```dockerfile
```

-	Layers:
	-	`sha256:fa324f4563bba4f1b5e8bf6dfac63e2c19b3d54e389c94ac161f7de7e6bc5944`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.6 KB (140590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe221b196f9139c99e479c14b73b286f065f2f9ab7233d397462f48bcba7b1b3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.9 KB (18862 bytes)  
		MIME: application/vnd.in-toto+json
