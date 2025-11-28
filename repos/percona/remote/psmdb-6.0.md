## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:2d482818c658f8babc84680a8052d5c71ea3c45eb1118694223b4e8db4610f06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:14c2442f66377a7fe320f72c86f11c734dca4a7fd20fc0fe789c9a9aaf6d972d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254998613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e71ca6308650b23464fa1a264ad8ea7381a787ac8f1869b4b810b7d0857195`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Mon, 17 Nov 2025 23:16:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 17 Nov 2025 23:16:18 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 17 Nov 2025 23:16:18 GMT
ENV PSMDB_VERSION=6.0.25-20
# Mon, 17 Nov 2025 23:16:18 GMT
ENV OS_VER=el9
# Mon, 17 Nov 2025 23:16:18 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Mon, 17 Nov 2025 23:16:18 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 17 Nov 2025 23:16:18 GMT
ENV PSMDB_REPO=release
# Mon, 17 Nov 2025 23:16:18 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 17 Nov 2025 23:16:18 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 17 Nov 2025 23:16:18 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 17 Nov 2025 23:16:28 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 17 Nov 2025 23:16:28 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 17 Nov 2025 23:16:28 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 17 Nov 2025 23:16:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 17 Nov 2025 23:16:29 GMT
ENV GOSU_VERSION=1.11
# Mon, 17 Nov 2025 23:16:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 17 Nov 2025 23:16:30 GMT
VOLUME [/data/db]
# Mon, 17 Nov 2025 23:16:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 17 Nov 2025 23:16:31 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 17 Nov 2025 23:16:31 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 17 Nov 2025 23:16:31 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:16:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 23:16:31 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 17 Nov 2025 23:16:31 GMT
USER 1001
# Mon, 17 Nov 2025 23:16:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c69b3b34d1a6eb888543a8b5dc763707508c4d98c96c9aac730ce1d6373e4bd`  
		Last Modified: Mon, 17 Nov 2025 23:17:08 GMT  
		Size: 8.8 MB (8812963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cacf6d84c8802fe6828cae5355dbc4bb64fdacce5ae81d3a674f57edd601a0`  
		Last Modified: Tue, 18 Nov 2025 00:11:22 GMT  
		Size: 205.3 MB (205253347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c7eac137d06ff05375d644faf24bf88dceb90451784476f121e3edbb2ae842`  
		Last Modified: Mon, 17 Nov 2025 23:17:06 GMT  
		Size: 1.7 KB (1665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb111c54f9f019eadbef536d26c147e021bd19d546e51a7d1153e52692ed8d4`  
		Last Modified: Mon, 17 Nov 2025 23:17:06 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679ea803e6e65c88a734ee05ad8d6331f03eb028d6068420b24c5b7825b4f467`  
		Last Modified: Mon, 17 Nov 2025 23:17:05 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688731c303950fa23a43d54f86904e8e3471c6e3b64616a96d87c64ce271cf8c`  
		Last Modified: Mon, 17 Nov 2025 23:17:06 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03cfceae32b308d54e00707ad5f8b8eea8439ed56eff5711879187125bd46a0`  
		Last Modified: Mon, 17 Nov 2025 23:17:06 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b488a6ec2b10def01d8ed054ddd5e7abfbaf9bb14f0e423feb9b126fa9730b2a`  
		Last Modified: Mon, 17 Nov 2025 23:17:06 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb94ff53a28f3e4a163570bc8bf6a474c6d528353d0fd06e4cce78db7d2e8b`  
		Last Modified: Mon, 17 Nov 2025 23:17:06 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:92201acb7a0e5d73c1b5556fa564d19cd8b9c2f7c346f0e7b3b3af1e9f300e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aade2029e37b1eb9f421d17e88daf2498b3cdbb2a331802bb7fc43e6ee0495e`

```dockerfile
```

-	Layers:
	-	`sha256:1fb95d664f6e7bcad4653cea8d9829f3e6e6cef1bd3ae172552892c0b150e3b1`  
		Last Modified: Tue, 18 Nov 2025 00:10:43 GMT  
		Size: 32.8 KB (32777 bytes)  
		MIME: application/vnd.in-toto+json
