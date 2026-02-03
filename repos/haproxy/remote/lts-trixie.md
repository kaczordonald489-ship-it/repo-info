## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:72106e05d64f24a3957619b22df66c17812f92a91fca91435897ce6e99bcc8c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `haproxy:lts-trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:10c5cdd0d91e6466dd6464dbdfd6e80f29bcc99dd39829fa62bb13b478ff5e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44490498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8af1f577703ee9c400bd19af5785e190d26846707c51672b5da4ce81f9cae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:17 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:16:18 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Feb 2026 02:16:56 GMT
ENV HAPROXY_VERSION=3.2.11
# Tue, 03 Feb 2026 02:16:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Tue, 03 Feb 2026 02:16:56 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Tue, 03 Feb 2026 02:16:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 03 Feb 2026 02:16:56 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Feb 2026 02:16:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:16:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:16:56 GMT
USER haproxy
# Tue, 03 Feb 2026 02:16:56 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Feb 2026 02:16:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9691071c99290c4737100ad43c4582d6414c479c5d67bdce0b9235672300e379`  
		Last Modified: Tue, 03 Feb 2026 02:17:03 GMT  
		Size: 1.6 MB (1580825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a659d1d0ad5cca1b3941c820d6f055b9b5800420120ef2ea3899d3f22f817a9`  
		Last Modified: Tue, 03 Feb 2026 02:17:03 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1053ee83f2bb12d773b3e31635b3ccb990e9827a866fa37e15bb24150c2dc5cf`  
		Last Modified: Tue, 03 Feb 2026 02:17:03 GMT  
		Size: 13.1 MB (13129436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95dd8ff1bbcec8972c938b255be56c3f496131446934e1f07514dd7769a30ec`  
		Last Modified: Tue, 03 Feb 2026 02:17:03 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0a2e5155b4765923d50f2f8345b4dc43a91427c5736193ab3b1b6bd46c5d7f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a972071f439f8b91e8eb94eefc32c5d74ff1bc7a96c58121945fe61aad23efe9`

```dockerfile
```

-	Layers:
	-	`sha256:f7b288782e85f33013c1199c5f8069ce15ebc22eafb723d6c6341eb57028c5e3`  
		Last Modified: Tue, 03 Feb 2026 02:17:03 GMT  
		Size: 2.1 MB (2113770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e369743e9610791bdec50d9e8926404dc9fea5ef705234e77b47dedc5161abbd`  
		Last Modified: Tue, 03 Feb 2026 02:17:03 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:7c5bb4e1cc077bf0fc130b4ededbfd87b0c23d90ba7f0e2d88976a632617e39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42753052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50e9c95911f25b079bfc2053f78324f924c92db462372c059cddb44705d0947`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Feb 2026 02:16:53 GMT
ENV HAPROXY_VERSION=3.2.11
# Tue, 03 Feb 2026 02:16:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Tue, 03 Feb 2026 02:16:53 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Tue, 03 Feb 2026 02:16:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 03 Feb 2026 02:16:53 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Feb 2026 02:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:16:53 GMT
USER haproxy
# Tue, 03 Feb 2026 02:16:53 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Feb 2026 02:16:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ad548e55123186b5669a1f697c5464a907b2fe0e4f45640cc9d96072cc6913`  
		Last Modified: Tue, 03 Feb 2026 02:17:01 GMT  
		Size: 1.5 MB (1534849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9474618ee839c8ef3b05e6ae064323e69dd8c056c3a2188f96d10994d79890`  
		Last Modified: Tue, 03 Feb 2026 02:17:01 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49339bd5b85fc6cc38f24f7320ab369c36cc111a75cf9cc8af23fc6200b0100`  
		Last Modified: Tue, 03 Feb 2026 02:17:01 GMT  
		Size: 13.3 MB (13269006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27078ada5220bf8f1b1f9058dc25c52243f371a0fec3596757019836f2a92098`  
		Last Modified: Tue, 03 Feb 2026 02:17:01 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:03138f50d0ca8442162df893a7e55165cdb3f5ff61d92ead25f000fe8495fa5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaede7d37687f2ad0e76dc98f0f61adb67c35d3cb9bdbaaf91b68e78f994093`

```dockerfile
```

-	Layers:
	-	`sha256:2fee2309b02122d047deafa8954039f5b29650920f5d72468aa9d8eb4d4ce24f`  
		Last Modified: Tue, 03 Feb 2026 02:17:01 GMT  
		Size: 2.1 MB (2116750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ee78c4e9da324bb09bf41749439102de9fea0c475ee86a99bc1589e8efb293`  
		Last Modified: Tue, 03 Feb 2026 02:17:01 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:47cd310da5bd27466a0632f504f6894a3b0dd7cb18b9f750f9272cc1dce7e425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40726030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6373a8d47c8402dde3a5f9a1c28150e8560df943b54ba8d020ececb3987680b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:10 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Feb 2026 02:18:26 GMT
ENV HAPROXY_VERSION=3.2.11
# Tue, 03 Feb 2026 02:18:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Tue, 03 Feb 2026 02:18:26 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Tue, 03 Feb 2026 02:18:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 03 Feb 2026 02:18:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Feb 2026 02:18:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:18:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:18:26 GMT
USER haproxy
# Tue, 03 Feb 2026 02:18:26 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Feb 2026 02:18:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec1245d5b524789766a1e172acebbec4d410650154e4810f87fc8dcad5eb3a9`  
		Last Modified: Tue, 03 Feb 2026 02:18:33 GMT  
		Size: 1.5 MB (1488901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262752a6a7a08f3d7f5378d26c51f211af4f7292df3b9a46b6873e8a1ee2a7ba`  
		Last Modified: Tue, 03 Feb 2026 02:18:33 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c5d5c2936e6740e648cb84b28bfec23480d5dfc12703bc21ab48e5814f90ac`  
		Last Modified: Tue, 03 Feb 2026 02:18:34 GMT  
		Size: 13.0 MB (13021738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5cfd5ded1d88dcec4ffd8f133d570040aba00086c35a2c6e302187919aaa8`  
		Last Modified: Tue, 03 Feb 2026 02:18:33 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:4dddb93ca90248834d948595d8f2a8d233413219a5d97b36f3c4fbc3dc3a75fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ae786e41f8554f5dcbb0e4ada8ce744297a90fecb912e27982195f7d7768cf`

```dockerfile
```

-	Layers:
	-	`sha256:2f8ad0248bf24bd3fe9a55b2fe5816404267571464091d319921be28cca8aea1`  
		Last Modified: Tue, 03 Feb 2026 02:18:33 GMT  
		Size: 2.1 MB (2115193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232cdfd347e57bcc1094ac1d2b044b66d37adb371e505a0dd107a109dcd2bbfc`  
		Last Modified: Tue, 03 Feb 2026 02:18:33 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f4e6e5ed072c0d363de662a7b9b6af214f8b9daf0e448529c395774d9db6923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44740022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c381000c0e368b5a7e868f7be266979925cf126b66610e83a2b4391be7f6ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:06 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:16:06 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Feb 2026 02:16:49 GMT
ENV HAPROXY_VERSION=3.2.11
# Tue, 03 Feb 2026 02:16:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Tue, 03 Feb 2026 02:16:49 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Tue, 03 Feb 2026 02:16:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 03 Feb 2026 02:16:49 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Feb 2026 02:16:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:16:49 GMT
USER haproxy
# Tue, 03 Feb 2026 02:16:49 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Feb 2026 02:16:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea70cdd1db2d308a14fd65b1da1d43da634e3a1e38be101cc9717cdfd416f0fc`  
		Last Modified: Tue, 03 Feb 2026 02:16:56 GMT  
		Size: 1.6 MB (1563094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb64387367a2ecd214639680d4b0747e5786269261a3e9e4a8d7fd29062a671`  
		Last Modified: Tue, 03 Feb 2026 02:16:56 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720503f12572a6a8c8dad28561bce0874845904f851ae67222bb45d172f284f2`  
		Last Modified: Tue, 03 Feb 2026 02:16:57 GMT  
		Size: 13.0 MB (13035223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edc608a515ea0d7cb5a8cf29182ea17fa13e7982bcc808bc9beb6992ca8c8e7`  
		Last Modified: Tue, 03 Feb 2026 02:16:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:d24a1cb441de168fa83217a91c14cc7d7458aeb04851ccf9223cd6084ef7a52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b53ebf34c60afdc6df2b2044198d82ecd11a21bfbc30263b9349749b428de8`

```dockerfile
```

-	Layers:
	-	`sha256:cbabeb82259ab23ff74abcff2e7ceb5db18c2e00d261eaa51e44779fd181009e`  
		Last Modified: Tue, 03 Feb 2026 02:16:57 GMT  
		Size: 2.1 MB (2114055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748450b16627e59da9d590a5148b4e8e756cdf96d448f3bc78f9ffac5a87edfc`  
		Last Modified: Tue, 03 Feb 2026 02:16:56 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:1d13a36d0e48c4072ac4288128b3b531cc6650a56916a616503ab031f570e31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45717983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d792bc693abd54f2808b1bc23c52a2bb4cbf6e9dfd8957dd37ab667b27d1c953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:21 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:16:21 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ENV HAPROXY_VERSION=3.2.11
# Tue, 03 Feb 2026 02:17:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Tue, 03 Feb 2026 02:17:11 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Tue, 03 Feb 2026 02:17:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Feb 2026 02:17:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:17:11 GMT
USER haproxy
# Tue, 03 Feb 2026 02:17:11 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Feb 2026 02:17:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc489484410a733e6383cab06f4b84c92f078a966424d79bcfb5c8c0fe4389b`  
		Last Modified: Tue, 03 Feb 2026 02:17:18 GMT  
		Size: 1.6 MB (1603104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f04aa641edda4b12337890586d36bab9f4aeec081b52251db1b3b62fcb29071`  
		Last Modified: Tue, 03 Feb 2026 02:17:07 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379277b17830b9ff7499e35c8ef18d2c9269eb48763bc85b3d72c31f093fce`  
		Last Modified: Tue, 03 Feb 2026 02:17:18 GMT  
		Size: 12.8 MB (12819382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d47f12dcb21687975e4448e7f6bf0ec7d90d95ade4e87f635c13640c5302e4`  
		Last Modified: Tue, 03 Feb 2026 02:17:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:7aceb3285b54c7ea50ec2cb5de61539e7a664bdeb2bd901a79c5579b5c536256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a9af979a317d1a211b4b5bc887ce304861ebb5ee96c9f183cf7d84b2472707`

```dockerfile
```

-	Layers:
	-	`sha256:a43a53b7ccefa96681b8a6e41fd9713507a21c7bae4243683a8feba38610d938`  
		Last Modified: Tue, 03 Feb 2026 02:17:18 GMT  
		Size: 2.1 MB (2110951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99e21f1a5763119f330dda9895399da53bbcbc297f810bbb0c93ad198057b1a`  
		Last Modified: Tue, 03 Feb 2026 02:17:18 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6edeb747ed48c6dce113bbf3fa474caa077dfa5202789f3401794343e6d663cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49049162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4c9b53994caf88096a11c02583e600fa9469200907d3a5536db13b08fed476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:32 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:16:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Feb 2026 02:20:11 GMT
ENV HAPROXY_VERSION=3.2.11
# Tue, 03 Feb 2026 02:20:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Tue, 03 Feb 2026 02:20:11 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Tue, 03 Feb 2026 02:20:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 03 Feb 2026 02:20:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Feb 2026 02:20:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:11 GMT
USER haproxy
# Tue, 03 Feb 2026 02:20:12 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Feb 2026 02:20:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb771c91e68e5c0b2810027274efd76c7432c5f533c9a2accab194ad66eeb7d`  
		Last Modified: Tue, 03 Feb 2026 02:18:36 GMT  
		Size: 1.6 MB (1638768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c41ab1963e36afe1baceadf478dee292e798dd968ef46b581c8352941f3ca25`  
		Last Modified: Tue, 03 Feb 2026 02:18:36 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a85e214b216641d12b6124ba577f69f933081dd9ef583f3f927b76d6fd55c3`  
		Last Modified: Tue, 03 Feb 2026 02:20:27 GMT  
		Size: 13.8 MB (13808569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726aa44730503938561b04a216098cd3dc3e71db18843ebfb611589510c5ad79`  
		Last Modified: Tue, 03 Feb 2026 02:20:27 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c2585d4be3810c1c3fe640faee68e6e219a2633f91669c750aa68e40da209fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655c326a4eee94f59f10f20a6f800da8df43bc3e8a68f893030c7c26a9b23c0e`

```dockerfile
```

-	Layers:
	-	`sha256:d9361d4aec11b53bb90f11c275d21b6e9698ed521f79a74ea9e2dc6b82aa6f69`  
		Last Modified: Tue, 03 Feb 2026 02:20:27 GMT  
		Size: 2.1 MB (2117316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11a1573edcd7b379b6bce06eecb75af1174a2baf96593dbaf085e3b737c6ca8`  
		Last Modified: Tue, 03 Feb 2026 02:20:27 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:41dc12ea9d11b0fac189fe58f714e548845b43cd4bf21d8320098b74ff775c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45567845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7920c04b789ebb84f0ae5d50f9bc7ac013989968864df822568ce865cafdb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 23 Jan 2026 10:39:05 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 23 Jan 2026 10:39:05 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 30 Jan 2026 19:07:01 GMT
ENV HAPROXY_VERSION=3.2.11
# Fri, 30 Jan 2026 19:07:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Fri, 30 Jan 2026 19:07:01 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Fri, 30 Jan 2026 19:07:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 30 Jan 2026 19:07:01 GMT
STOPSIGNAL SIGUSR1
# Fri, 30 Jan 2026 19:07:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 19:07:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jan 2026 19:07:01 GMT
USER haproxy
# Fri, 30 Jan 2026 19:07:01 GMT
WORKDIR /var/lib/haproxy
# Fri, 30 Jan 2026 19:07:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51baf30350568c1d52b41b999c74c716c2743ae62fecc93c4e834d424070ee98`  
		Last Modified: Fri, 23 Jan 2026 10:55:53 GMT  
		Size: 1.5 MB (1535180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a514c90374245593cf14dbe5a3d6c00292837cc1cfd4b032000953c7cb5cf`  
		Last Modified: Fri, 23 Jan 2026 10:55:53 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d50aa0cfd693c2e92fe7ccd268c4b1b83ad3e103b0fbdb4359d3e03cc523fb`  
		Last Modified: Fri, 30 Jan 2026 19:08:10 GMT  
		Size: 15.8 MB (15759334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe213f6b2b689705badf8569b84e5887faf09d60b4389058221cc52b5eb2437b`  
		Last Modified: Fri, 30 Jan 2026 19:08:08 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:6cfb06c5b64cac1c695461a2a0ca3897c74c3b1dafe9c0918469d61c8386f12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fe952e9f5ab70fa8c3d2ce2cfb4472d4e4fdb051bbe1c62b22eabbc4591c49`

```dockerfile
```

-	Layers:
	-	`sha256:0d43f5d16316923a0d15b9fc4ba0b27cde7fbf9bfb3cbf667651d3740cd26505`  
		Last Modified: Fri, 30 Jan 2026 19:08:08 GMT  
		Size: 2.1 MB (2107707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3519988ba98f0736cdb0a64cdc325b0959cb0bf1d22983d1b04b471516f718cf`  
		Last Modified: Fri, 30 Jan 2026 19:08:08 GMT  
		Size: 22.4 KB (22408 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:b29e0967bebb5aad62efd3441be4687bc1cedef124d70bdf3b859aef381779e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44862024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d9e00ad7dfb07f01974d4dbfa189c278db463b0301ed74f76bcb7f5845c285`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:20 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:16:20 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Feb 2026 02:17:33 GMT
ENV HAPROXY_VERSION=3.2.11
# Tue, 03 Feb 2026 02:17:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Tue, 03 Feb 2026 02:17:33 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Tue, 03 Feb 2026 02:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 03 Feb 2026 02:17:33 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Feb 2026 02:17:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:17:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:17:33 GMT
USER haproxy
# Tue, 03 Feb 2026 02:17:33 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Feb 2026 02:17:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fab5145002df87b755c3365ffe5d31d9c023f2030be231ac20e687c4cf405fc`  
		Last Modified: Tue, 03 Feb 2026 02:17:45 GMT  
		Size: 1.6 MB (1599661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4551f1effe7320dc0344a5632a0e30de254c50e901234090139596658519e583`  
		Last Modified: Tue, 03 Feb 2026 02:17:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95f95c7189a172efe91a1331ee91185ee8e29fe55dcfe7e879a1541cd8195ec`  
		Last Modified: Tue, 03 Feb 2026 02:17:45 GMT  
		Size: 13.4 MB (13422573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816bcbc58a38d7e311cfb43b678df9e028f743098948809a73214d53264d011e`  
		Last Modified: Tue, 03 Feb 2026 02:17:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:b5be21a674192fac09394b8e07733a619768191afc87c6d4496a18e809f53614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8cff0bb373f721a0d79c9a26646be35600cd95be906d04d67cbcf1e913af66`

```dockerfile
```

-	Layers:
	-	`sha256:086eba86df1e0d04649ba943f7290791c7556e072cd45021e614d5048f325383`  
		Last Modified: Tue, 03 Feb 2026 02:17:45 GMT  
		Size: 2.1 MB (2115214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa960bf15ebae85cae3af9c0fc070d6384eb5a209250570f25ee66ec9ce5074b`  
		Last Modified: Tue, 03 Feb 2026 02:17:45 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
