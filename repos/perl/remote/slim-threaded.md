## `perl:slim-threaded`

```console
$ docker pull perl@sha256:8a4526cd0f78cd7718f0cf28e97c18bba237fd50a0edabf1359cbd5aaee8b53a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:1e7a5ab22f57038fc36383ad6551cb36ee3356d08e84211f78e0b83a2b9d42db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61787983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa9d71c029a30241ca6449d3872e42b209e80f1ac6c4ae57171d6f4c3f3c7b4`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:36:16 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 05:40:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 05:40:56 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 05:40:56 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a1e0bfb9c3f90d1c5aa8d21485b054a8574a0dae3c1dc58b62f5798f2a8dfc`  
		Last Modified: Tue, 18 Nov 2025 05:41:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3aafb1a11f827f3a714c0b463aa891bdf76d5ac3735b6a3c163d254bc331cf`  
		Last Modified: Tue, 18 Nov 2025 05:41:16 GMT  
		Size: 32.0 MB (32011234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d29fad0b22f99547da97d2508189dbee4de504a4b28f2ecbdd27e8b06da950`  
		Last Modified: Tue, 18 Nov 2025 05:41:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:2144f44c03eb0817b5f1a226502e32591e19e6486a7afc8290ab4897a922c3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650db1491a7ac94025264aa4db9039c5a193b6c48c387bd37afbe30e945522b9`

```dockerfile
```

-	Layers:
	-	`sha256:bf5a90fe7c4b0def9656bb38a1e09a29e803e1c7890895b8e2bd2f42537931ec`  
		Last Modified: Tue, 18 Nov 2025 08:38:42 GMT  
		Size: 4.0 MB (4010658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187e2efdb00275b29cab17d1f528e51b83dedc32da6ccf6ee692e29df5f0cd62`  
		Last Modified: Tue, 18 Nov 2025 08:38:43 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:b6e8f1a829ada1a7b70dde0e624b083e90ab5486e242ae14e7eac9fd236ba676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57167590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4fb92cbf567990fbe89735caa3b974175adcd741ae754e236ad1803df830a1`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:38:03 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 03:44:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 03:44:03 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 03:44:03 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca89fc24e55c27a1da273ff684ff3de5d51532496d4cd6373389ba5fc5f92201`  
		Last Modified: Tue, 18 Nov 2025 03:44:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa76c12963fefec25e13f4495d9eb0b98fbeaaaea9f7898df3802ff609647f45`  
		Last Modified: Tue, 18 Nov 2025 03:44:22 GMT  
		Size: 29.2 MB (29223178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da6fe9a2ee637e6e2be2c00a3ce8a6ee746ad361816fb607aa3f35cb4bed04`  
		Last Modified: Tue, 18 Nov 2025 03:44:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e078c1b0de4a738447bd0501bbe113fce1a18dcb880be36b258f530afcf6650c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869d8acae946f8e9a476f5f22b38c04b04b9ea581fd6bc1aa4408b57d6f0233f`

```dockerfile
```

-	Layers:
	-	`sha256:bd12ac28a85837f5bce22dc0a325862db2d014913e2b16a027901f2783253259`  
		Last Modified: Tue, 18 Nov 2025 05:39:21 GMT  
		Size: 4.0 MB (4003735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87923dfa0d4c058a8bfd23595c16e9fe1aa69b671ce29fe90072881b47692017`  
		Last Modified: Tue, 18 Nov 2025 05:39:22 GMT  
		Size: 20.6 KB (20611 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:82f1aa97fd6c10391afef4a58ff459583aa42d8c948ed9d9cd957fde370f17ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54512518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03888935c76cfa40a32295f8fca60a43106478e3f7946f9d03d39ceae4ea337`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:25:11 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 04:30:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 04:30:52 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 04:30:52 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c153550ee5cefd8160009efdc0d794c96285e3450625ac948262664c1d7e73`  
		Last Modified: Tue, 18 Nov 2025 04:30:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc694ae7bfc7f880e915d77b3ef87207f1aee925bb14c52498f56d3a93d0f31`  
		Last Modified: Tue, 18 Nov 2025 04:31:14 GMT  
		Size: 28.3 MB (28302291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b541d7708615ee655ece87c995e8bc390d7a89bf71d372c75013e74e884ed2`  
		Last Modified: Tue, 18 Nov 2025 04:31:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:c2242d0e9da2ddda7c7391e5b6f17fe29bd5484f906523f2f22388260682dd7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c181dbfd83de1794d86afae8323be04ba7862ba376dd2c856eef5f072bfdd5c`

```dockerfile
```

-	Layers:
	-	`sha256:49ed71e4fa0ecbef51c9044154b91af913f317deac8814bd052647aed6a6835c`  
		Last Modified: Tue, 18 Nov 2025 05:39:26 GMT  
		Size: 4.0 MB (4002926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3ead444f3b577725d8a67851cb0fdd08eebb1bd4a9c9cd2b3d688fb4192093`  
		Last Modified: Tue, 18 Nov 2025 05:39:27 GMT  
		Size: 20.6 KB (20611 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1984bd798146f4f341553ca7818beec3ef52167a4176d318d9743c6c27a473af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61804177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d277d54dcc9bda84d71ae7c82662b35cfdd16e91433d8b8e039fcd338f46ee4d`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:48 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 04:19:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 04:19:35 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 04:19:35 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15130fdf6577e9bc2e592e9e74b5f3b7e4b5812ec6e024993e41eed79a2f30b`  
		Last Modified: Tue, 18 Nov 2025 04:13:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6ac0bda3fd3d75b4aaab6215de6282104ed12d3a6f913aedabc81dfd82df33`  
		Last Modified: Tue, 18 Nov 2025 04:19:55 GMT  
		Size: 31.7 MB (31665301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e004de465e9a69b6c997a361bc6b8800ee791f89fa7c837eb8ca3beec304f0`  
		Last Modified: Tue, 18 Nov 2025 04:19:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:0d6a44efa229fd222bd1dc02f444c014c9657357ccc9ca4606546db901de6051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977410adc2eb86df5e551700d34189386d0b984aff248a0597a896e4b42a425`

```dockerfile
```

-	Layers:
	-	`sha256:f083b7ac172150d7d1992bb119f3d9b12ac1c4b91f017c254ee2ed703a3fe40e`  
		Last Modified: Tue, 18 Nov 2025 05:39:31 GMT  
		Size: 4.0 MB (4005801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13edb6084066fd363d39fbcb78fc2697a45e637cd0d95374b9119c55e43c1b02`  
		Last Modified: Tue, 18 Nov 2025 05:39:32 GMT  
		Size: 20.7 KB (20659 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:f54dc75445523beaac2d0f6e8bdd6d92b9582a2a1ed9a903484805579de67954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66366845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001c73b173f83b7c0a2538e9507542cf8d9387503086eb821d05c48112e7ca96`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 17:13:28 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 17:22:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 17:22:31 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 17:22:31 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caffa0566b7ffc49d2b55d11b33ada2f32d38bc79833eca75e3bdd1fc2c69a4d`  
		Last Modified: Tue, 18 Nov 2025 17:20:57 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b992f9f958d2396db2c62d124afcdda0757a931c0da2b9044b101c4311f6fa`  
		Last Modified: Tue, 18 Nov 2025 17:23:26 GMT  
		Size: 32.8 MB (32769721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb4db82198ddd94cae52de24fc16794c67a7795d5d650adbb6dbeac2218002d`  
		Last Modified: Tue, 18 Nov 2025 17:23:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:3feb14a6f1d9610dc061c2c40cf1c1cfc46cca59f1e080886a3b4fe99ed99ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4027257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d45a8112a1eed49fe4313d6d29f4d383c2a7ef7ae8b0c07da576473e370ae04`

```dockerfile
```

-	Layers:
	-	`sha256:c9f3607ed8695432954af9f0294fe438e496c9543686f3dbea13cc73ead2a647`  
		Last Modified: Tue, 18 Nov 2025 23:38:06 GMT  
		Size: 4.0 MB (4006694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd0ad058d587b2b4f5a09faf1e5524b425b15d369e3bc66060dcc8cc33c0c09`  
		Last Modified: Tue, 18 Nov 2025 23:38:07 GMT  
		Size: 20.6 KB (20563 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded` - linux; riscv64

```console
$ docker pull perl@sha256:475ae66aff197d0f13b9755a5f9947a9cdb382ebc3411fd4ddebd50c7d9ed3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68082055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc5074ed7b6ac8a4b0de510bc46c37a7a9a40b1efec6bc377cb7d9aece5f6ba`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:46:07 GMT
WORKDIR /usr/src/perl
# Wed, 19 Nov 2025 22:10:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 19 Nov 2025 22:10:30 GMT
WORKDIR /usr/src/app
# Wed, 19 Nov 2025 22:10:30 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6928c7e45a6fa759c436ba0c58b6a512d4cad42edd79bb3f56b5ca1813ced5d4`  
		Last Modified: Wed, 19 Nov 2025 20:56:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcfd86af6d8bcc2a96a9584f12b71ae3185bcc540b29d3b353c13680bb561fd`  
		Last Modified: Wed, 19 Nov 2025 22:13:17 GMT  
		Size: 39.8 MB (39808662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10014b71904d5397e24e1e38b9648322412a3233e929da5453d2701c2ff0184e`  
		Last Modified: Wed, 19 Nov 2025 22:13:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:eb0c996daac0d07b320bb75140abb053c5fe4b294d7f1e2f70f98df75afafe14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4018523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf293cb866a0877802c47bff4e0219e2664841b5f8bddcedaa9aef1816974766`

```dockerfile
```

-	Layers:
	-	`sha256:6151736bb1a1206c83816731e5de601370271c7bc335f006fc057c723cbcec9e`  
		Last Modified: Wed, 19 Nov 2025 23:38:33 GMT  
		Size: 4.0 MB (3997960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba911a2a38a2955ac12fd900091ef43a7128f65d5bf1c4025960fc7f1e5a9372`  
		Last Modified: Wed, 19 Nov 2025 23:38:34 GMT  
		Size: 20.6 KB (20563 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:slim-threaded` - linux; s390x

```console
$ docker pull perl@sha256:727a78de613ae324db5903fc3e360022992f274a28c0b9dac514b756037fc1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61186051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bb48ee48cb155065dec0138cafc748df0fbf782ce63a4767c57e53c737ab2c`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:14:31 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 04:20:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 04:20:30 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 04:20:30 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606695f08f26553c27b321edc2320d379d4a4e37b4868fdd057c106d3823754`  
		Last Modified: Tue, 18 Nov 2025 04:20:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6520aa5e02c588fae02881a395d11a9dc94b11fe3771f49055083e39d2204abf`  
		Last Modified: Tue, 18 Nov 2025 04:21:03 GMT  
		Size: 31.4 MB (31351413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31dab1f82304ae95230ed3193abca751faa3a5c7cc8b5c7316192d2f742a80c`  
		Last Modified: Tue, 18 Nov 2025 04:20:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:slim-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e0959bfe30deec21b0345f503fa33b88d612aa9f82cf4f809c38eb05615d00f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4023469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb017fde16648ef6a75aa72a0be85ebc7776e8a5eb6d57d50a239f21a233415e`

```dockerfile
```

-	Layers:
	-	`sha256:fea10be13b8dcfa09cd43c0bb2639e3a11fbea03380093734ed746d83bde89ae`  
		Last Modified: Tue, 18 Nov 2025 08:39:02 GMT  
		Size: 4.0 MB (4002986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c529a53d892d45430a404843a0d3a265587ab0b5b6e279c19cb0bdd70d4b146a`  
		Last Modified: Tue, 18 Nov 2025 08:39:02 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json
