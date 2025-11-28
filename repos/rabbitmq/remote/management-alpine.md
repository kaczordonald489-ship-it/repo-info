## `rabbitmq:management-alpine`

```console
$ docker pull rabbitmq@sha256:4c158536d8a1688c1bcf58573403471168542ecf5da914bb460eb36248e914b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `rabbitmq:management-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:ad187ef6af7fa03c3170f6b32afe28bff2dfaafee6c036246566c4b272a66ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97176495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013c1914c40bdbc64bc52eec8053357fad314a51349b9f5c04ff1d86df5e315c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 02:57:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 02:57:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 02:57:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 02:57:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 02:57:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:57:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 02:57:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 18 Nov 2025 02:57:13 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 02:57:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 02:57:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 02:57:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:57:20 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 02:57:21 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 02:57:21 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 02:57:21 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 02:57:21 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 02:57:21 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 02:57:21 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 02:57:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:57:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:57:21 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 02:57:21 GMT
CMD ["rabbitmq-server"]
# Tue, 18 Nov 2025 05:59:41 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 18 Nov 2025 05:59:41 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa64c726c0d1f5afec7e7f5cf026ec8f1349980314b54d7999bfc37b8d0ce70`  
		Last Modified: Tue, 18 Nov 2025 02:57:48 GMT  
		Size: 42.9 MB (42858211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce5959031876c0aa0f8dd8210e1a12792bfe797af579501cc31d421db454005`  
		Last Modified: Tue, 18 Nov 2025 02:57:47 GMT  
		Size: 9.1 MB (9143878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13d352d48737ef0a972a846db6e40d8966dbee220a2601a7017d07697ecde8`  
		Last Modified: Tue, 18 Nov 2025 02:57:46 GMT  
		Size: 2.4 MB (2374341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c93c87d509c802d802949ec1b0abc4fb23d19794ca25212faceca25e5d638f`  
		Last Modified: Tue, 18 Nov 2025 02:57:48 GMT  
		Size: 25.3 MB (25282798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8032671c652c2e6464d89385d7d6efc57a7925e94f9a1398c44da39af78542`  
		Last Modified: Tue, 18 Nov 2025 02:57:46 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5843846f85bcf653f88180858634f4420c892df985f16189e8efee2de6ee0`  
		Last Modified: Tue, 18 Nov 2025 02:57:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b2a192d24afa9b05e2255f06a67a2414d5d9a533c3938fa032a5b5d6764108`  
		Last Modified: Tue, 18 Nov 2025 02:57:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a95c245e7e1c4f10dcd3cd896c0d8d1e87027ce379537bb7adf932d4cc4f604`  
		Last Modified: Tue, 18 Nov 2025 02:57:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c8b3e6920d1482c50abe0dedf8191dfb25699405f5ad521b35c2a283f4513`  
		Last Modified: Tue, 18 Nov 2025 05:59:54 GMT  
		Size: 13.7 MB (13713069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:39a6d6a3c3598ec612157f927a8d96c03720e60f7a183fbe7ce472b15a49f855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1661187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ee25a78e7d5be57afa783260ca5a7b648bee349d8f24b9dc702a9194e84a02`

```dockerfile
```

-	Layers:
	-	`sha256:82aa7dd5ad59c442b313672667a2caed481e69b5262d36f6c1f9b685fbc7263a`  
		Last Modified: Tue, 18 Nov 2025 07:53:35 GMT  
		Size: 1.7 MB (1650007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c273f2c9015a2ba20c4160e2789d45fb11d319467e657e5a73200c2422d722`  
		Last Modified: Tue, 18 Nov 2025 07:53:36 GMT  
		Size: 11.2 KB (11180 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:bb77d575a5df2a6a04f2cc8319f52d8b5e4f0afe79d87dd5d5f98ca3feafae6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85746284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99bc95a061803e3e24e9057f7cf3b7c593349caf929bc2a9b972dddc4a5264`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:02:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 00:02:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 00:02:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 00:02:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 00:02:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:02:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:02:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 18 Nov 2025 00:02:53 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 00:02:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 00:02:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 00:02:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:03:02 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:03:04 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:03:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:03:04 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:03:04 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:03:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:03:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:03:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:03:04 GMT
CMD ["rabbitmq-server"]
# Tue, 18 Nov 2025 00:10:02 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 18 Nov 2025 00:10:02 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2028d91319177ddc90f1652226a3dd356a4c800dc8882dd3ae2e0fc463c363`  
		Last Modified: Tue, 18 Nov 2025 00:03:26 GMT  
		Size: 33.4 MB (33447830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e2b3738711d2c255ca6c956226c36239abccced961fc6b52c71a600f2f8cc1`  
		Last Modified: Tue, 18 Nov 2025 00:03:20 GMT  
		Size: 7.8 MB (7788809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b59056d7c5c97d280a34f5da8a938205c8ca1faed8553af49a592888b358bd`  
		Last Modified: Tue, 18 Nov 2025 00:03:20 GMT  
		Size: 1.3 MB (1330035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0cc49a4b1ef2d74d280ef3d6d79e085de7806a2cbda2b1f6ec1e792b45cc77`  
		Last Modified: Tue, 18 Nov 2025 00:03:23 GMT  
		Size: 25.3 MB (25282558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5df0dd762f8f327ac58e71613c11ed18916fc196fadbc47a34dcddcaed4e1`  
		Last Modified: Tue, 18 Nov 2025 00:03:19 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db6480c6fd1a0f14a2fd6b61ac8034d28ec8ecb7a3758d72f76c22a9f1158f6`  
		Last Modified: Tue, 18 Nov 2025 00:03:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cead3562025b18cfe4fb960a090a5f788094fdae80b53807f2a3a939a10baa`  
		Last Modified: Tue, 18 Nov 2025 00:03:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621d98d5e93c8d9fca1d6b849a1afbfe1fc00ccb2ec70839875d2b8a35a2b1ff`  
		Last Modified: Tue, 18 Nov 2025 00:03:20 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6346033a09a4efd34dd8515a4e849835309afe3e4be5528df105fa9364f08dc`  
		Last Modified: Tue, 18 Nov 2025 00:10:14 GMT  
		Size: 14.4 MB (14391228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0c943cb9c261f4bc155d956d3f3ef0cd6c203f705f94a4ff39172b22366e6eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 KB (11045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed3922e5b11a8d9f1e077cd645604537d5ea28282a8322cb34122e1a1cc719`

```dockerfile
```

-	Layers:
	-	`sha256:ea302039c1482aa73711d592e5a7207ffc1e91c5a106904bb5ef48f4be96f3be`  
		Last Modified: Tue, 18 Nov 2025 01:53:48 GMT  
		Size: 11.0 KB (11045 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:e256fe1a8e9e8eb1fdf026467dde7d9496e18c15cf699edf0b1ce2dcfa9e6bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84574005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbe2e1ea239e727ba01dd6655b05b7df88079b7159f88e235c0174f7d49f9a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:02:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 00:02:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 00:02:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 00:02:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 00:02:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:02:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:02:04 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 18 Nov 2025 00:02:04 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 00:02:04 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 00:02:04 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 00:02:04 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:02:10 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:02:11 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:02:11 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:02:11 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:02:11 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:02:11 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:02:11 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:02:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:02:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:02:11 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:02:11 GMT
CMD ["rabbitmq-server"]
# Tue, 18 Nov 2025 00:09:17 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 18 Nov 2025 00:09:17 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97923e3f5cd29faaa1dfb7caa934afd465fa13ecda0caa54416b10c77249f3b3`  
		Last Modified: Tue, 18 Nov 2025 00:02:41 GMT  
		Size: 33.4 MB (33392530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713e5ee45589424de0ac757c264cafcc8032b0898f7e4f4e72e136cc7d89c5d9`  
		Last Modified: Tue, 18 Nov 2025 00:02:39 GMT  
		Size: 7.4 MB (7390494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116dab853822e3c2baeeb9595d38574e8790766cb14ecd6ba7bf0eb4af319ddd`  
		Last Modified: Tue, 18 Nov 2025 00:02:37 GMT  
		Size: 1.2 MB (1227056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789cf04ecf707e921903cf6f04b791e54618018beab3a17cb8dc79470e4f0db`  
		Last Modified: Tue, 18 Nov 2025 00:02:44 GMT  
		Size: 25.3 MB (25282056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7290bafa7c3adca6f04ddfe313e86e890df65ebb40dfa50662cd5df2ee8d6ace`  
		Last Modified: Tue, 18 Nov 2025 00:02:38 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2e37682df04b6b610d088300a5ed63ae5a36a118e284c3538ad399f315765b`  
		Last Modified: Tue, 18 Nov 2025 00:02:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cff64e6b4a06d6e10d3bfe7c355dd5fad1ebe0f7797d87018317692e31b88bf`  
		Last Modified: Tue, 18 Nov 2025 00:02:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c2a171dc35c2f19a19a6344a828c13d510d09f4bcb59a79111299a07390e97`  
		Last Modified: Tue, 18 Nov 2025 00:02:38 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9cb324ba1b298c9dd9fca3e10e8b950ec54d516cfa55e472863a40d8d29f7a`  
		Last Modified: Tue, 18 Nov 2025 00:09:41 GMT  
		Size: 14.1 MB (14058567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e9bf836eef83b2d61ac34dbc3445fc3361b4c279dbf75a1837bf271100f5f0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4f0c2d78912de05e3e958d2020b1d2c9370959e8e541dd4906c72b8e4c9b3`

```dockerfile
```

-	Layers:
	-	`sha256:7e46caeaa6b66811f3e12432336e53db09e05a85036ff49e5958d82cfed9a938`  
		Last Modified: Tue, 18 Nov 2025 01:53:52 GMT  
		Size: 1.7 MB (1651038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3848ce46a7ba3740710f0be099d3f63dd8e4ba5a114e39f8720547feb2bafff0`  
		Last Modified: Tue, 18 Nov 2025 01:53:53 GMT  
		Size: 11.3 KB (11259 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:fb0d3518b7ebb01b6b21f7c087ceaf67d8d503d02da21379b3ae564dd78d29fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96271012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4158745b661667b3ef5e39d91d547bcfdb0a6224318dba8f62d44cf57a99e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:00:38 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 00:00:38 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 00:00:38 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 00:00:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 00:00:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:00:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:00:41 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 18 Nov 2025 00:00:41 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 00:00:41 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 00:00:41 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 00:00:41 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:00:47 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:00:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:00:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:00:48 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:00:48 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:00:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:00:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:00:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:00:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:00:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:00:48 GMT
CMD ["rabbitmq-server"]
# Tue, 18 Nov 2025 00:12:11 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 18 Nov 2025 00:12:11 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99905281f3537095c6acd121b3623c51b63a564c00fe6bd725fc9ce6cd778549`  
		Last Modified: Tue, 18 Nov 2025 00:01:57 GMT  
		Size: 40.9 MB (40854400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbe0887d9d1baa3e12e344967664f3db937775c4823171cbb54c3ba96422ce`  
		Last Modified: Tue, 18 Nov 2025 00:01:49 GMT  
		Size: 9.8 MB (9824246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeed570e555b718404348c23c6939912c02e6248c6e84faa932531bb229757de`  
		Last Modified: Tue, 18 Nov 2025 00:01:47 GMT  
		Size: 2.4 MB (2424795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11044a126b8898f6d6aef3c14bf809954056d8bc54ce03d906a8324a60553e6`  
		Last Modified: Tue, 18 Nov 2025 00:01:50 GMT  
		Size: 25.3 MB (25282679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da1d86a0c3dd8a698e737d2ff063b35135f1ef5c7485c28b496864833874b2a`  
		Last Modified: Tue, 18 Nov 2025 00:01:46 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a735883f4a174bbe2452cc970232da879e1a8aba532f5795023ba85814ba4`  
		Last Modified: Tue, 18 Nov 2025 00:01:46 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fbd225f82826813a4a8e5ee8a869338e3bb41eac9f584ee000b00614a04632`  
		Last Modified: Tue, 18 Nov 2025 00:01:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fdcbc60bbcf4b8561baa62e1fb81f434131237e46a817ce35e1acf334b704a`  
		Last Modified: Tue, 18 Nov 2025 00:01:46 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69833cb11900b4491c6213f1c5a7386deed08cd17a6209fe8f0c58ebd73264fd`  
		Last Modified: Tue, 18 Nov 2025 00:12:28 GMT  
		Size: 13.7 MB (13745080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9af50e9430f597253b85740fd0fb8df3e69345d4c3be737673b7a0c9fdc04a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5518aaab9c89893e157ec1eaead36885b5b950126fefbe5a80c214149ca0e2`

```dockerfile
```

-	Layers:
	-	`sha256:033dcafc46670d94d6937641a4e650fd750a54703fdc1639f229fcb5d9592a51`  
		Last Modified: Tue, 18 Nov 2025 01:53:56 GMT  
		Size: 1.7 MB (1650886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22bee2b84eda89fcd0ec1261070a4cb13293f6482d73ee95d95fc4827d43449c`  
		Last Modified: Tue, 18 Nov 2025 01:53:57 GMT  
		Size: 11.3 KB (11284 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:271d95871da5349a611ccbf7ce7459ee0398b13b85fcaa85e741ca15729ed6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88163193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653a384cd6d06358135d955b4303f34150221664d2e34f33d9722b1df77ae71c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:02:05 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 18 Nov 2025 00:02:05 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 18 Nov 2025 00:02:05 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 18 Nov 2025 00:02:05 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 18 Nov 2025 00:02:05 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:02:05 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:02:08 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 18 Nov 2025 00:02:08 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 18 Nov 2025 00:02:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 18 Nov 2025 00:02:08 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 18 Nov 2025 00:02:08 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:02:13 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:02:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:02:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:02:14 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:02:14 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:02:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:02:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:02:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:02:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:02:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:02:14 GMT
CMD ["rabbitmq-server"]
# Tue, 18 Nov 2025 00:09:23 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 18 Nov 2025 00:09:23 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae5b9f5d86910671fad0268b5f6fc9ee44d123308c241f678aae4920228a5b`  
		Last Modified: Tue, 18 Nov 2025 00:02:46 GMT  
		Size: 33.5 MB (33537216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2968e323905547224023eea09392f500da0a4e5a5f79c00a04e806440102be`  
		Last Modified: Tue, 18 Nov 2025 00:02:43 GMT  
		Size: 9.2 MB (9159134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77590470d1e37a57ad5a97171cc40520047423c6b08f19dd54e56297a41eb97`  
		Last Modified: Tue, 18 Nov 2025 00:02:43 GMT  
		Size: 1.3 MB (1332462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17824b1070e6f346aa4aa69d822bfbd088aaf0bc765e530867f06158cd654f3b`  
		Last Modified: Tue, 18 Nov 2025 00:02:46 GMT  
		Size: 25.3 MB (25282056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d7cd040a87cf7685f4711797ac3f304f692c2201ee2a8fec0ceb698c736392`  
		Last Modified: Tue, 18 Nov 2025 00:02:42 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad636f3ea5068ad7235589d3433cdf6419d111df45148fe5bb57775d988d9cd`  
		Last Modified: Tue, 18 Nov 2025 00:02:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347a0b8bff3c6463162eedfa27314015abbaa8abfba9a6ab209e549c64f72a41`  
		Last Modified: Tue, 18 Nov 2025 00:02:43 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873247213291f640decdc80171f0534cb32e4ce6fc5c954b888c8e0c1d1cc741`  
		Last Modified: Tue, 18 Nov 2025 00:02:43 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6393b5654c02ffa7f79bf5656ed21b4db4b2cc104791672e85684a113fbd8235`  
		Last Modified: Tue, 18 Nov 2025 00:09:47 GMT  
		Size: 15.2 MB (15231648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3b6d7debc00141156198fc936a8fdebfa77e5ced7ece0fcac178c22e7bc67fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1660957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d593a176076a5e0c126ec5398513b4e1f7463bd366135586d6c6048fbb67c9`

```dockerfile
```

-	Layers:
	-	`sha256:e0d440020795058ddda5759225f01ecf34b803faed57f8a1e69e61726fc5f917`  
		Last Modified: Tue, 18 Nov 2025 01:54:01 GMT  
		Size: 1.6 MB (1649810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a91d1d7720353e60c523f910da82877d543665c179c093432bbb3f7c0972bc`  
		Last Modified: Tue, 18 Nov 2025 01:54:02 GMT  
		Size: 11.1 KB (11147 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:5c0635f550f481cb7c4f6ca765aa32b6ab091f38b1b6575bc2cc7360bb245cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89560882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616560eb0961e805ed923b7e43667bf23e2719e1c41318c5c3f3fd1a1f380e11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:14:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 19:14:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 19:14:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 19:14:43 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 19:14:43 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 19:14:43 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 19:14:47 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 19:14:47 GMT
ENV RABBITMQ_VERSION=4.2.1
# Fri, 14 Nov 2025 19:14:47 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 19:14:47 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 19:14:47 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:09:24 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 00:09:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 00:09:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 00:09:27 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 00:09:27 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 00:09:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 00:09:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 00:09:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:09:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:09:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 00:09:29 GMT
CMD ["rabbitmq-server"]
# Tue, 18 Nov 2025 00:22:37 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 18 Nov 2025 00:22:37 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaa900e9d6ef3065872bc442df1a96294cc331aafa72563993a7cbc9248e799`  
		Last Modified: Fri, 14 Nov 2025 19:15:53 GMT  
		Size: 33.9 MB (33928492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4e1eec0ae82c73bec5eddf8d6bd090fc1bbc1bab910a01b6fb17f3bee11d6`  
		Last Modified: Fri, 14 Nov 2025 19:15:51 GMT  
		Size: 9.8 MB (9774080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494003fd5d13a10f29866599f6b08e4fa4c468ed3e29dfef022619deddd86cf`  
		Last Modified: Fri, 14 Nov 2025 19:15:50 GMT  
		Size: 1.5 MB (1452640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca6326cfeb3a6163087353cd666cbc31adf58a6db35fa775fa8cbeb43aa81d9`  
		Last Modified: Tue, 18 Nov 2025 00:15:26 GMT  
		Size: 25.3 MB (25282151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce12df85657c33af3d758367dbdb858efcfca7510841f0920b09b549ea130ebe`  
		Last Modified: Tue, 18 Nov 2025 00:15:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65a933cd1be5fb4dbdadf57c3dd7e4e090941f104e809108201148151414f39`  
		Last Modified: Tue, 18 Nov 2025 00:15:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0c7f868b61ca6de19efb4751b0836a5dd73f61547b9b65efdc116979796ed3`  
		Last Modified: Tue, 18 Nov 2025 00:15:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7786d55cd427bbbc6e3b85b139c445c3a33c2b527ff3021f96ba691cbe32dc`  
		Last Modified: Tue, 18 Nov 2025 00:15:23 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c95328020081d7329392a7e03aeab06d0a4539789ef9c9791a19fa3d87761d`  
		Last Modified: Tue, 18 Nov 2025 00:23:15 GMT  
		Size: 15.4 MB (15389525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9bef07c01be8c27e3fee816d1c54a5c1b511ca78c2f79bc0610117f90d6dad39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1660480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e9dc39e86865abb5c2209ee6d97b35bf7713bb58fb52f2143c41ff5b99e421`

```dockerfile
```

-	Layers:
	-	`sha256:4a52145505e4fc74eb988b49a8bfe46887c748afb5e9cbe2680cc782372b0e85`  
		Last Modified: Tue, 18 Nov 2025 01:54:05 GMT  
		Size: 1.6 MB (1649257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f346256ed691f6170104a1c9b5e90488e363aaaf2cb2f35a2782f7d86e52c0`  
		Last Modified: Tue, 18 Nov 2025 01:54:06 GMT  
		Size: 11.2 KB (11223 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:5e1ed18a1c10db5a68f6eb8effd472eb64d0cf383eb274019a31740e36ad4de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90831499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75abd0d7dd624a9da79bdd9ba43ec23a5fc6d6aeb21914cd2aa3c05da5f69d7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 15 Nov 2025 12:40:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 15 Nov 2025 12:40:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 15 Nov 2025 12:40:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 15 Nov 2025 12:40:38 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 12:40:38 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 12:40:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 12:40:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:20:39 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 03:20:48 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 03:20:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 03:20:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:20:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 03:20:48 GMT
CMD ["rabbitmq-server"]
# Thu, 20 Nov 2025 12:52:07 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Thu, 20 Nov 2025 12:52:07 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e59a1c1b9f6e68d2e81dfe93f128277d090e8d42bb80d9fdce1bd0812253e90`  
		Last Modified: Sat, 15 Nov 2025 12:47:29 GMT  
		Size: 34.9 MB (34892992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b82b64d03f44428bb7c7c84bc38b196743066f1c2cd8073fa6e2958a1f2364`  
		Last Modified: Sat, 15 Nov 2025 12:47:25 GMT  
		Size: 10.9 MB (10906598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445ba2528747173700141a982a31baa29e2bb537c0faf37187397c5cef3d8ac0`  
		Last Modified: Sat, 15 Nov 2025 12:47:24 GMT  
		Size: 1.4 MB (1366487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ab85becded663592a6bc65df027d3b64784a81fde022e9ef0f2d593a067f8f`  
		Last Modified: Tue, 18 Nov 2025 04:39:50 GMT  
		Size: 25.3 MB (25282651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c6b0a6f4b731df4b2017078d1d133e2cbed722a0bca6e74485cc38e59b447f`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e1906d3f3c215386290a7ef260fba1c1a172ded9261e1333dfc67ea58d0473`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f065a8e08b979e6b746f95b8f4fc2e86e14d9b444bf9212b642e4e55b9c3833`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb79fb793b07ee339d044a1fe1e5e3f5dd9213f52951f7d84366dd805ae73a`  
		Last Modified: Tue, 18 Nov 2025 04:39:47 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d997ea765508a356554758e5e5068cfbe70b85c309f0f2f21167dbfea9fac`  
		Last Modified: Thu, 20 Nov 2025 12:53:36 GMT  
		Size: 14.9 MB (14865778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1979464f3fe0dbde6bfffe6c4bbefa1836f798aaeaaa1ded26ee7c0c4c003585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a79adbdca31ce4e36fb5f39094faf488cf36ba199d8298c65bca0476430fc37`

```dockerfile
```

-	Layers:
	-	`sha256:fbea5d91c3c0d912cf6497df4214394f212d25277397393208ad88c0106d5133`  
		Last Modified: Thu, 20 Nov 2025 13:52:53 GMT  
		Size: 1.7 MB (1650866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3005df4217fe90ddd0d8548e07ea0120a83f2a4889f9e5850f91af773a3570fa`  
		Last Modified: Thu, 20 Nov 2025 13:52:54 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:593c73ea918292e8c910862994b483ca94321d14fcdb6e1021dd39967229e4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88071241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea7ae5b4f183e02e0f589697b5d49b0cb08365613b8b69ce6d8f0d33bdff788`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:32:33 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:32:33 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:32:33 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:32:33 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:32:33 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:32:33 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:32:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 14 Nov 2025 17:32:36 GMT
ENV RABBITMQ_VERSION=4.2.1
# Fri, 14 Nov 2025 17:32:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:32:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:32:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:57:43 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 17 Nov 2025 23:57:44 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 17 Nov 2025 23:57:44 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 17 Nov 2025 23:57:44 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 17 Nov 2025 23:57:44 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 17 Nov 2025 23:57:44 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 17 Nov 2025 23:57:44 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 17 Nov 2025 23:57:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 23:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 23:57:44 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 17 Nov 2025 23:57:44 GMT
CMD ["rabbitmq-server"]
# Tue, 18 Nov 2025 00:09:39 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apk add --no-cache python3; 	rabbitmqadmin --version # buildkit
# Tue, 18 Nov 2025 00:09:39 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf19dc786e7146ac66f96833a9722c5bc83d7ddc7799ab6e6f8872ac24ad163`  
		Last Modified: Fri, 14 Nov 2025 17:33:23 GMT  
		Size: 34.0 MB (33963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc957cadda9e73e64de07d656462cb108e148515232cbc504b1a8ff8af5678`  
		Last Modified: Fri, 14 Nov 2025 17:33:22 GMT  
		Size: 8.3 MB (8347174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8c2fb2646dac35cf3ca4279dce3c3af62715ef5a7d8541e9faf78b85cd28d3`  
		Last Modified: Fri, 14 Nov 2025 17:33:21 GMT  
		Size: 1.4 MB (1430636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fad425e02a82294a38ec6999c50e1cfd76cfd41472d458f36f9830f62ab32c`  
		Last Modified: Tue, 18 Nov 2025 00:05:29 GMT  
		Size: 25.3 MB (25282226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd3e9c83a23b8e066d74dfe4e90a150c83b8ce2b8c1001b333f8deb1286178a`  
		Last Modified: Tue, 18 Nov 2025 00:05:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09faf6053fd9260a03f7e4b4f8a1f9487e11c169c5ea4071b16df3fcdc18eab0`  
		Last Modified: Tue, 18 Nov 2025 00:05:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9ed7074e02f02115448c0e92fd4f46c8d9cca6a390bb906f4eb6ded682aed4`  
		Last Modified: Tue, 18 Nov 2025 00:05:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919a4ac8016b9935c83fed29310037e0f68ed51f9ef21d63230ee38ad1cdd7b8`  
		Last Modified: Tue, 18 Nov 2025 00:05:25 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326c238640d8da9af003158df3af7666bc0e1ec5a108a71cf53ddc6c2a808f93`  
		Last Modified: Tue, 18 Nov 2025 00:10:01 GMT  
		Size: 15.4 MB (15396507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:34934760b5591c90d5379e0c06c1b1ae9a311d30e6fc00d873cd73a863263aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1659887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9009cba2a972168bc7bd7b9342ca0ab1e900105a793ab7dbd2eeb59073d3b1`

```dockerfile
```

-	Layers:
	-	`sha256:0f37abf13923a94c93f9962615aebfc7a454d119886f913ebadf307336f36cdb`  
		Last Modified: Tue, 18 Nov 2025 01:54:12 GMT  
		Size: 1.6 MB (1648707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7180252c0aa436d82f7e8306688d7909ad1871ba71294f371a2eac6c5ff41a`  
		Last Modified: Tue, 18 Nov 2025 01:54:13 GMT  
		Size: 11.2 KB (11180 bytes)  
		MIME: application/vnd.in-toto+json
