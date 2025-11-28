## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:71968ebd8d6bde3d1972068ec3a05fe4a508300b787970d6372252b5e6354735
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:581a0f0778e150f6e982df9c81e9bee235d1f43f11a1bbf1a22cee4b15759b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255734788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da724aa7115c97027fc0e515354e5bd47834c65e5c5238ed910ecb21e9056ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:13:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:13:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:13:47 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:13:47 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:14:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:14:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:14:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:14:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:14:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fb004a71cdf274c3185a648c9ed1285f37e7028b36e4e18b431704a09a9265`  
		Last Modified: Tue, 18 Nov 2025 07:58:59 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07d16a4e591383630cfa67b7ce66534df13bf7737e8b3cc1ac0d76c6896bb2`  
		Last Modified: Tue, 18 Nov 2025 06:14:40 GMT  
		Size: 69.7 MB (69679270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697e8960ba4a1e611f327323dacbb2f77c236a10d2da72285db37dac75ebbc5d`  
		Last Modified: Tue, 18 Nov 2025 06:14:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0b427019e8b9229de110a26451d85ff4c5a3dfd56515e1da881512bc43cf20`  
		Last Modified: Tue, 18 Nov 2025 06:14:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc983aa637dfd349b251e6b1594ac1991e3508bce8f73b3abf58487b958c08ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a50c31ab7d8e84300a1293a8198a04da32cb54f15fc98d6c5cec51a173f5ae`

```dockerfile
```

-	Layers:
	-	`sha256:34b0aad1fb48ca631e6aaefa5692a5f0fbca6bc7bb8350c29c9b194356fa3bbd`  
		Last Modified: Tue, 18 Nov 2025 07:44:01 GMT  
		Size: 5.1 MB (5116492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da942d606f7e82ef417b191ab55835621fc8d672d876b0f1cf4c84342a41e36`  
		Last Modified: Tue, 18 Nov 2025 07:44:02 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:10c5a7a860d2295be6a70131f5cb83c72f060906f1b7f75902c3d4e224c3e723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253771296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503bb45b64e6a06d4251c0b7b2483ada01e954b72b5d53bc4d3915009a3f2f0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:09:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:09:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:09:23 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:09:23 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:09:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:09:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:09:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:09:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:09:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387c3beb6f7150989e84cd78e7bc57da02f2509deaf62af9335927ee470b621`  
		Last Modified: Tue, 18 Nov 2025 08:02:14 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b29d26c6208cb1d34185c528ceffa87502e868beaa44c72640cc4e803bbdef`  
		Last Modified: Tue, 18 Nov 2025 05:10:17 GMT  
		Size: 69.6 MB (69560469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52543733d7e1c9a99dd160761de85a888830ddd49a56f7bd078c68558e7e253c`  
		Last Modified: Tue, 18 Nov 2025 05:10:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc7f688ba56907c8f7c81638f8d5f6ad2cf04d8d447b50de8f5aea64787b28b`  
		Last Modified: Tue, 18 Nov 2025 05:10:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4cde82706dafab94fd39de245fd5701e312701d096d2a45b3b47d56aa736c2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f5dca87b9e6150e542e90da212cdced6943b4df2b10eb43cccc60a189a87f7`

```dockerfile
```

-	Layers:
	-	`sha256:ff8a67bce373cc656ed8138862dcc4125add4ae39bf0034889241d03f3ef52b6`  
		Last Modified: Tue, 18 Nov 2025 07:44:07 GMT  
		Size: 5.1 MB (5122253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7c85aae35d7158346340b9c9023768103458a3829a27ac8a1a922cc3675611`  
		Last Modified: Tue, 18 Nov 2025 07:44:08 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2ae7dabc3bda8844ae958901c2e44461b6ceaf457788adb3ea378024cd10ff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265526122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3a419b6a93a09d204b0df496886597c00d5fa865d4e2957bee7dde1356242a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:34:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:34:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:34:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:34:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:34:19 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:37:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974478515d7c186335e22d66c2a7dde61bca42ba9c7978f9a54fbf628ade7ca`  
		Last Modified: Tue, 18 Nov 2025 08:02:48 GMT  
		Size: 157.9 MB (157942922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4503b2ddf64ea7f44fb9fb6be5f40b58f2aa317b9388950a6b4b74dae881b02b`  
		Last Modified: Tue, 18 Nov 2025 06:38:40 GMT  
		Size: 75.5 MB (75513333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15be46da2523e4fbe25eb13b78962e4e353d36835cbbd3254679fff4a99d2175`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8778adeb60495f3113e54d5370e9e61dc5cb5686d82dd0c816af7bfe200631f6`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46b89c6908c26c1cb8141377a9f768861f9f1602a51362675e5b68ee611b5b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdd41cfbfcf63ea0b0fa9934eea962f46ae24939070031be7061304b090907`

```dockerfile
```

-	Layers:
	-	`sha256:fb2ff3ea6f073111497425ea8110b37962915c3167e2781b67ce9880ca2611a8`  
		Last Modified: Tue, 18 Nov 2025 07:44:13 GMT  
		Size: 5.1 MB (5121650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145d12eb66157be1003913f0a499abf5dd4fd30620742600ffbd97d63c7debb9`  
		Last Modified: Tue, 18 Nov 2025 07:44:14 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:67174587f3cece6805fd74e697e22aae24e20ea2307d80f6556b5726263fcf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242445808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcb6a278989f6fd12c43db4d85fdb77696a752b7531bf40d6959ae20bd4ad8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:29:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:29:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:29:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:29:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:29:10 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:30:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:30:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:30:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:30:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:30:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415602b41fe29f565cb6f40bc115c3f7a4f54bc07ed4e0df0facd0f20103746`  
		Last Modified: Tue, 18 Nov 2025 08:03:21 GMT  
		Size: 147.1 MB (147069811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c8ccb91e0aa5b2494daa8836231851c7bd75761873c238b68db37095e222af`  
		Last Modified: Tue, 18 Nov 2025 05:31:32 GMT  
		Size: 68.5 MB (68490562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a9a516e9e51d1349d1bd122137b9092e0adcb5042320f30c713d3261075d39`  
		Last Modified: Tue, 18 Nov 2025 05:31:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78fe1c71c99080254f954d1e20afd947f179dbc0440b199ef9d58eab2f111b9`  
		Last Modified: Tue, 18 Nov 2025 05:31:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5fda2dd02e4b5f8be2556be061269497f711f3060c7b371077e93cfccd966b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d63df305997c05a4de94551a929d1559fe21d0d0ebb178dae73a279258d010`

```dockerfile
```

-	Layers:
	-	`sha256:a5977af9f27cbf89bb66076d7ddc7a369c1a514e7aaae5c40685b6b18a3cc5d6`  
		Last Modified: Tue, 18 Nov 2025 07:44:21 GMT  
		Size: 5.1 MB (5107813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f908070d1521e564fda4c772dae3d5ae2e713b884becdbb1e60dc71c63ef54e`  
		Last Modified: Tue, 18 Nov 2025 07:44:22 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
