## `perl:devel-slim-bullseye`

```console
$ docker pull perl@sha256:ff44da30b4d7b33dd9930f427344ac03bf5e538e86103baca69a89d6e496be87
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

### `perl:devel-slim-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:54c8b15a9f1fab485ce7edadffc7b276048417eb5bfb3193588f3a8caf2ba86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56629000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af42d0089e608f4eb8ec2fc5cabf25ccbceda2396f5dceef7514935ee6cd0d27`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:59:55 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:03:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:03:49 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:03:49 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d040cacdf3a70de80680be646e1a163abbb1db62544b5ef212d1b055eaf45`  
		Last Modified: Tue, 03 Feb 2026 03:04:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf9ab7b88f0ea8082d081406dcb44a88ca27f7bd366e69ab80cb9d09ea8e451`  
		Last Modified: Tue, 03 Feb 2026 03:04:01 GMT  
		Size: 26.4 MB (26370448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493bc13ed6edf8af29e7df596e14f14dd977937ed79e85a1fd658bd92dd62b05`  
		Last Modified: Tue, 03 Feb 2026 03:04:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:708da58b6c674f20dca05a6280a1827a03025169d23cc16b1de9f6253ba6f861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a582a83af2774474131eaa7401c7af59d7f6b00893e95a7cd19f9466beaffdd7`

```dockerfile
```

-	Layers:
	-	`sha256:f4a9796f840bba450cb09e068a6531ee3b7eb8f25c2e19f4588cd20e06fc9ae5`  
		Last Modified: Tue, 03 Feb 2026 03:04:01 GMT  
		Size: 4.1 MB (4120643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87a52be8168aa581dd302ec65066a1459508ef8a6058f57a683a07284b9b60e0`  
		Last Modified: Tue, 03 Feb 2026 03:04:00 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:e18ae6e4eee19f4d5978728169e45ef0c031290a217063b711133ae11c9e0c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49174951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c8ab550761c6e15565e45b0e7f528b66fed3fd31d335b37fb5230daea10f6e`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 04:14:45 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 04:19:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 04:19:58 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 04:19:58 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:944e0be0007ce5fe7e4b3a40294acae7be162c471fe44e2e543c304ac6eaf2c0`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 25.5 MB (25546109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce5b937d617d503c304f9ce63490f73e286ce75fd450c5f3bcc972d29aa4dd3`  
		Last Modified: Tue, 03 Feb 2026 04:20:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f565d148dd3fcdcd2b18cd3e280a8ff6c5eacf73a4540ddded69407fb41bbbe`  
		Last Modified: Tue, 03 Feb 2026 04:20:09 GMT  
		Size: 23.6 MB (23628574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75abc0ab774d05aa9f1258f816275028ef20e6df5e9a690915f0f1827b58d32c`  
		Last Modified: Tue, 03 Feb 2026 04:20:08 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:23fc03ebf2699757a52426526d6aa83e2ba6321d052c9d5b8748ea43f7f1574c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a371b0d9ab2807d38a41180966d49a53f4186281f70ca5a8f563f8e35a5aee77`

```dockerfile
```

-	Layers:
	-	`sha256:e4a3c40a5915df876dcb00edb5240bf2c9fd1dfa6809fe4e1dbbd1ae3cdb4df8`  
		Last Modified: Tue, 03 Feb 2026 04:20:09 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0697817f2c97a400a255fd66390e3ce4826e10e29850dacbd34942ad3e5bcf`  
		Last Modified: Tue, 03 Feb 2026 04:20:08 GMT  
		Size: 18.3 KB (18316 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:d9763cf6e079230b47b29e178a223627011d5c855814a6f5c716c393d03e732b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54251179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e2d7a2a6434a1f5d61f5699c9ecbb2150458abe7c3734b405792687f55d545`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:59:18 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:03:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:03:50 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:03:50 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097b9b6a80416a576b766905e955ac424c2dbcb106d3bbe23ef90142b6b7cc1`  
		Last Modified: Tue, 03 Feb 2026 03:04:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a12132f4392bd6f54f83500ad205f8403e56a20843f1cb2f406e4ff790961`  
		Last Modified: Tue, 03 Feb 2026 03:04:02 GMT  
		Size: 25.5 MB (25506474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d0c23969fe8b85872a81453c7605f15ab9a7d2285936fe43b961319315601c`  
		Last Modified: Tue, 03 Feb 2026 03:04:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f7606a8d4e4a8a2121c075eac39b657971e831959e72ae0ccbbf50ee10ad6735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0872a2cf03255457ff6bb11840adf26f5ed94000fc3601db7122457dfd2356`

```dockerfile
```

-	Layers:
	-	`sha256:52f388c054bbf40d633dc8a8b6204465490654a73fdd6cf8fee282bd45d537c9`  
		Last Modified: Tue, 03 Feb 2026 03:04:01 GMT  
		Size: 4.1 MB (4095038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d75f2e228ce195495bd6ffab82c9fe22f832464333a78d77bbfa58e43076a3`  
		Last Modified: Tue, 03 Feb 2026 03:04:01 GMT  
		Size: 18.3 KB (18336 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bullseye` - linux; 386

```console
$ docker pull perl@sha256:ad903ee155a6cec32aeccdf995d7488f5888fa680056cfd2352dc4e98506955f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59071847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57796090f13d3fa646256eb189cff4bc156f98421186cd1e13ca2b0649bc94f3`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:50:59 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:01:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:01:26 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:01:26 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:be44e5b8c6651635597dcc56e16b6cbc27fa88aac451d0e6807ab115918f8351`  
		Last Modified: Tue, 03 Feb 2026 01:13:55 GMT  
		Size: 31.2 MB (31191501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c479f64ff6fa1284fbec9dd3056f0ab0e194ab5ad4dac1869f2f3a18b1bb22`  
		Last Modified: Tue, 03 Feb 2026 02:56:26 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba0a34640b6f8ae2601bfb16792b93efe9ad9ab9f93e8a5b5489d1e5630f168`  
		Last Modified: Tue, 03 Feb 2026 03:01:37 GMT  
		Size: 27.9 MB (27880077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf57a7c1ddbf968665a4c085f1a60beee0c0dee5f16430789b5f51aed8daa85`  
		Last Modified: Tue, 03 Feb 2026 03:01:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:f8a849d8dec20e509c45b4bcbe5dccd20ca96eb759fae3b4b6a5b828108b55cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ec4a78a353fd5b74aee5f6f9cbdfb36ed0cce2c753e8c3711b656646fbe9b7`

```dockerfile
```

-	Layers:
	-	`sha256:c435ee3f8fa3ca1c0b96705124b1c8542c7ecf5b99df1ed03e2aeb20caef9710`  
		Last Modified: Tue, 03 Feb 2026 03:01:36 GMT  
		Size: 4.1 MB (4124925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14cfaedd52278c596fb3663b285e006fdcebdd904d2a1e8e7e45f52a7d92334`  
		Last Modified: Tue, 03 Feb 2026 03:01:36 GMT  
		Size: 18.2 KB (18216 bytes)  
		MIME: application/vnd.in-toto+json
