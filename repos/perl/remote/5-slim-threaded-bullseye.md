## `perl:5-slim-threaded-bullseye`

```console
$ docker pull perl@sha256:da6aa6080e6f8f19a00bc7ba6ee8f2162ef7cd46492a92198b11bb1470d7d0a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `perl:5-slim-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:92baf7f54bc80bb838de79913eb4c1d48c55f855a7adee45913f50cd87541f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56485090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac56a556a4f5276ce61d67b3e374da79523c5ef6a9b18e1c77bd41d77696f6b`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:37:17 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 05:42:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 05:42:13 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 05:42:13 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf62a5045eca4185d79043602fcbb526f0a7808df7c0b6c3ab4ca4db5ef209ef`  
		Last Modified: Tue, 18 Nov 2025 05:42:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83958eea5bd7953af18e6fe62d3b60da66e381736da959a4ca6ba88b0857cd15`  
		Last Modified: Tue, 18 Nov 2025 05:42:32 GMT  
		Size: 26.2 MB (26226340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebdcd542b604e78a53ac396e92deb2f189895629fe8332a051adcff608ae1f8`  
		Last Modified: Tue, 18 Nov 2025 05:42:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:68da8b0dbf932e9626e979c7c646261e1ab777c11acdb507936226420c76e10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4959c4e73d44a580b629b20a172b409a35fd04dd183cbf145ff3a085444168b8`

```dockerfile
```

-	Layers:
	-	`sha256:0dcfc5193fbb3ed7289b383161127d18a5da24b5dd23dbbee3c6a5736e269e27`  
		Last Modified: Tue, 18 Nov 2025 08:38:58 GMT  
		Size: 4.1 MB (4121355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:351ca8a536063aab7c1b6b42e0c21593e7b591934e54b42dae7b6054038b4895`  
		Last Modified: Tue, 18 Nov 2025 08:38:59 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:98465d49b92c8220c6895d09993d9d8f22d2d8b1f104a102f095fd9df4169197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48994102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1922a03e86a4f7479319eaa84af5aabe1d3eec942a8f978c8f8c403be1eb264`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:25:33 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 04:31:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 04:31:16 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 04:31:16 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:31d48996d869b8f090a5e1e81c7a7bad23cfe63e84f9c8076aaac2db64d96fcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:57 GMT  
		Size: 25.5 MB (25546252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd09f40e2b83c240e10f0f94eef27f38236fdb7e7c8f0657172ba9d22f008ed1`  
		Last Modified: Tue, 18 Nov 2025 04:31:32 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5431180673bcefee55d6ab6462750b4eca51fb2792b228c7dd1143e693e6c444`  
		Last Modified: Tue, 18 Nov 2025 04:31:36 GMT  
		Size: 23.4 MB (23447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5acdd978750cccf5981808d07e6defefe5f6628786cd7dfc0837e59148d6d1`  
		Last Modified: Tue, 18 Nov 2025 04:31:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ff70e7b2d46d6d7f4920aa04af01468645ee14ca426c5186dc0109e6a551952a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1f7152534cfb2d50b9bd2c5ddc91ff6b7194772131a607e731e274edbfd9fc`

```dockerfile
```

-	Layers:
	-	`sha256:733685aaa83ee30a8efef210209332adde43c4beb730b84e24822dfe00d35482`  
		Last Modified: Tue, 18 Nov 2025 05:39:47 GMT  
		Size: 4.1 MB (4095360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7078902cdab8c5ae0962a36ac2c41641da64713e8dfc2aa3050494cbef2f77dc`  
		Last Modified: Tue, 18 Nov 2025 05:39:47 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:523be3ca9ee49e697d4c9a7039ced4224dd7831fa5490ac8ac9a9a41dc2573d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54089050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdd8798b51ff4dd5a2a42321ad4430329d498f51c784a3226d8984ebd2c5b68`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:15:33 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 04:20:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 04:20:26 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 04:20:26 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3445642d92a9b91d131eb44f9db4805dedd2108369499d8031ea00b4d64434`  
		Last Modified: Tue, 18 Nov 2025 04:20:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e753abfa890d33a1376fff3128ec62d753ee44c02242e4abf4303502444cd2`  
		Last Modified: Tue, 18 Nov 2025 04:20:43 GMT  
		Size: 25.3 MB (25340319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98554b4116ad630b6c4120f285ec716c6f4443d9a63055f07961dbc738a4a60`  
		Last Modified: Tue, 18 Nov 2025 04:20:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8faa6e1a0887e3c1cb8725f49b7b867f9f5af39d52fdff52d6113bf48b3cb92b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f57a6203adb81c57310529a154b2e8dd2abdf166bc7f86e1c2693330d64817f`

```dockerfile
```

-	Layers:
	-	`sha256:4601daad3ecc5c2c466e1c5c25bf948869cd59a643175bcd4fc870df49ebb056`  
		Last Modified: Tue, 18 Nov 2025 05:39:52 GMT  
		Size: 4.1 MB (4095774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c092bfa228136f697930161c1a861484d9510f4bc0d1dbf0fc376ae65192175`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-slim-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:dbb92f3af17a8421700acbb971ced2a5b1e03786625c945a6d2960709c635d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58971436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa647da58501a4434c62f35acfc57c75b38a8038de23f2957ad36d61a120be8`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:08:29 GMT
WORKDIR /usr/src/perl
# Tue, 18 Nov 2025 03:13:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 18 Nov 2025 03:13:38 GMT
WORKDIR /usr/src/app
# Tue, 18 Nov 2025 03:13:38 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:fa92431247d9c62b6c791fca54f16952c598cc5545329b6db7949cb86417c351`  
		Last Modified: Tue, 18 Nov 2025 01:13:18 GMT  
		Size: 31.2 MB (31191554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86764723f5aadad4d33f137ab1d54e18813ecbc4a001b33209a1f1ebe37f8979`  
		Last Modified: Tue, 18 Nov 2025 03:13:55 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00237fe16a7c4f0f92ad24730c6351957c06f8630b9d02615a4c28269e20d3dd`  
		Last Modified: Tue, 18 Nov 2025 03:13:57 GMT  
		Size: 27.8 MB (27779616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa022bc2a4bdd9f5a2810aa8a7abbfdf1902d83c46ee395541edf442c4fc29`  
		Last Modified: Tue, 18 Nov 2025 03:13:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-slim-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:58dbc03e18a8f50bba6126ff70701d0a06635dfa2c743035558e1705b8ac98b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4144517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a235c8d02250ce0d93acd78e4bc695c8680e2e75eae0173b48f2405544d89c1b`

```dockerfile
```

-	Layers:
	-	`sha256:d31d24bfe133a7e7a6e7c079e2275a81dacbd8abf4de8a31501b259cd73ff0e0`  
		Last Modified: Tue, 18 Nov 2025 05:39:57 GMT  
		Size: 4.1 MB (4125627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168860a380e36f5ff7ebafada03925c2ab8db2e5cf6a566b59d8f2a705df23d3`  
		Last Modified: Tue, 18 Nov 2025 05:39:58 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json
