## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:4350bf3a9723bbd767d84530688a73e9464ea32158e2f9d63081768cbd484dd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:f0e8da23f6825208d3cebcb2a889fa2482844f36b58ef2810acfa9f6990d8d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277188355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af568d0764c050721571f8d52a2d642c37a00a2a1cffa8ee18ad091cb4847ae`
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
# Mon, 17 Nov 2025 23:15:16 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 17 Nov 2025 23:15:16 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 17 Nov 2025 23:15:16 GMT
ENV PSMDB_VERSION=7.0.24-13
# Mon, 17 Nov 2025 23:15:16 GMT
ENV OS_VER=el9
# Mon, 17 Nov 2025 23:15:16 GMT
ENV FULL_PERCONA_VERSION=7.0.24-13.el9
# Mon, 17 Nov 2025 23:15:16 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 17 Nov 2025 23:15:16 GMT
ENV PSMDB_REPO=release
# Mon, 17 Nov 2025 23:15:16 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 17 Nov 2025 23:15:16 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 17 Nov 2025 23:15:16 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 17 Nov 2025 23:15:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 17 Nov 2025 23:15:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 17 Nov 2025 23:15:30 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 17 Nov 2025 23:15:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 17 Nov 2025 23:15:30 GMT
ENV GOSU_VERSION=1.11
# Mon, 17 Nov 2025 23:15:32 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 17 Nov 2025 23:15:32 GMT
VOLUME [/data/db]
# Mon, 17 Nov 2025 23:15:32 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 17 Nov 2025 23:15:33 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 17 Nov 2025 23:15:33 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 17 Nov 2025 23:15:33 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 23:15:33 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 17 Nov 2025 23:15:33 GMT
USER 1001
# Mon, 17 Nov 2025 23:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7d6ca59745ac48971cbc2d72b53fe413144fa5c0c21f2ef1d7aaf1291851e501`  
		Last Modified: Mon, 17 Nov 2025 07:24:40 GMT  
		Size: 40.0 MB (39979464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4531b2fb3f8888824ac3952b9f61edb92ddc5de300942288d0e10d9f776b9f`  
		Last Modified: Mon, 17 Nov 2025 23:16:15 GMT  
		Size: 8.8 MB (8810484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50bc28b53fb2eccb9c4e66b5e75d02f54a2b3ccd391f6a53cb8d4834419712`  
		Last Modified: Tue, 18 Nov 2025 00:11:10 GMT  
		Size: 227.4 MB (227445558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd84aaffb14bbad5bfc1204e9bb6719d0a5087e34d6fbec81469c9d57a6b408f`  
		Last Modified: Mon, 17 Nov 2025 23:16:11 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946ecabd5462009c25e140887ad0599caeead4d7f6a1d85dee7eed22589c7c1c`  
		Last Modified: Mon, 17 Nov 2025 23:16:11 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7ae632d9cf7874f74f6704710c8e5fa30f234d1123d77fd6d5e1be6b35d1f1`  
		Last Modified: Mon, 17 Nov 2025 23:16:11 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9bdcf7cd8cd6d064ace0e0b0a6270f55842acc21eb00dbaca866bf39253d91`  
		Last Modified: Mon, 17 Nov 2025 23:16:11 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5fee54818b85366a6f5abff47d7607fffd1fd8ec6a0df74468b5e005e8e10f`  
		Last Modified: Mon, 17 Nov 2025 23:16:11 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a6ad5bf6abe483be9a76f6e73e413ddf57b8e7fb40401d81ab3b7d71f64115`  
		Last Modified: Mon, 17 Nov 2025 23:16:11 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b86879820d20428debd753a03d814601490d1068e80de2e7f385db2db59eb1`  
		Last Modified: Mon, 17 Nov 2025 23:16:11 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:7b9ad83c19fce3c70189954a8442a1221513dcde46c675446c6133c29c9451ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef105b9d564ddc13dfc4bfdad9e9982c471a84a925fa77845b56ca14510aa78`

```dockerfile
```

-	Layers:
	-	`sha256:0094437417db230b9c2da63b05bf8a010d23539ef4ebf51e6386bd77ea7a0610`  
		Last Modified: Tue, 18 Nov 2025 00:10:49 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json
