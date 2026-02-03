## `debian:forky-backports`

```console
$ docker pull debian@sha256:dfc4996a3cb7c014c382889bf5ad32827ff321b8d95cb5601dff4caa9807d36e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:0b79bd9f24ef7a67d098bd9a2784deaabcc362a03fe6750fa370c1efb2cf1238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48655961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9397f052e5294c4ac4142fa5f5d0d6ddba0cc3b8d206ac34e7d49e78f3772427`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:16:04 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc5a63b4b43c1afff0d7421d031d0e005739a96950e6683e91164adbd846938`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:38361b0ba82c88b67ce88f327d0d4a8cb14936d0393c5821bf1b3b7b96d259c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe8a0cdd744e90841c5ee277d37ca61ededce1132c72154f3e6e81ffb125d84`

```dockerfile
```

-	Layers:
	-	`sha256:12e7a48b2fccdf8eddc2eaeb26382593426920acd048add83925f37da22e9eb2`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 3.2 MB (3150957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf2134bdb56937668417ebdaac24e9be81919ef0ecc2d14b4660449ba893f1b`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:32e2cb86508f56a6a35d16e1c8361bd376c5a75b3f6aaae3159e5aecc2ee40d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45620841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb4c7a1c4d923d3cac98cfd19830fd5a6a219f61a32edc690e83c457a68b0ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:15:48 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8ad4a919778d324780b6dee51af6abcf1139f6d57c0ba625c1995bf19d763478`  
		Last Modified: Tue, 03 Feb 2026 01:14:27 GMT  
		Size: 45.6 MB (45620616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5845421053ab61a14c64b11fe69546f82bfc5d24a144e2cb8f4db003521a3a1`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a2dbf4a2769b5c95538b80a32d92cafa59b0aa2c4c7c9e768e47c01cd4211695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ba84d66ad8e080bcecccb0b89cac2318295ed47a3e4ae5e7ffead584ef8106`

```dockerfile
```

-	Layers:
	-	`sha256:514b575037e8d507b3d0821026ff713e7d015e780ee83a43e2fb9f8a7bc57679`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 3.2 MB (3152325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c39832af4d7d2ccb87900014e537dc6c798bdef538eee616ff225cdb138319`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:39a4d96107cdfbb65ee4d422ea869e3223238fac13aa1337d6bc72af6cacd72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48678750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e346e4480886ed9cd961e2636bba84e13a342de8529330392067b26407e6fbab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:15:24 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2309f92dd0c61c985b2d0f865b8d146291a99f7a179b5a243da4f72d2cb33817`  
		Last Modified: Tue, 03 Feb 2026 01:14:24 GMT  
		Size: 48.7 MB (48678525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c232e15851558824bd20702e30dad3ee1126e5982099a4648028faee42a38d`  
		Last Modified: Tue, 03 Feb 2026 02:15:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f158855f4dae3249020de61783344be6703635712458c1e61d9215c4b059f00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf7f2d0a770bf55648b323d6c3edf5d932c73c6e691e208d884747b6d11ea4`

```dockerfile
```

-	Layers:
	-	`sha256:e9e2b4c9be7035d7eaf2e81cba4a8a533d4051b0d1d7909bc8465ead2b506195`  
		Last Modified: Tue, 03 Feb 2026 02:15:31 GMT  
		Size: 3.2 MB (3159643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d0aff2e0953383ce458e50ff0057c6c72b4bde52573c712128446cc257bb0e`  
		Last Modified: Tue, 03 Feb 2026 02:15:31 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:a2814b5d3e277cc65bc51c26a2c2b8498ba8fc65e05602e9f5971a05c20c2724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49982160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b8ba35e2d8646d33f1ccbfc00b26b865d42e19924c6a4997b4abc1bc3a2b05`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:16:02 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bd6304d6e56f66e13385dc7464436c6e3933118a9e5b697acc2b57e9b6d5e5cc`  
		Last Modified: Tue, 03 Feb 2026 01:14:23 GMT  
		Size: 50.0 MB (49981936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897e3fd31a8efa495fabfd3fd8fe9e8c5e1f8616c447c2126fa387991e68fe1`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0f56b10a671d387a2aba8bed38901d4c7eb5862af98379b712ac862bd12a57a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b5b9cc985fcc62c8fb8edde9398317ce91aa66f673eca88f9d96e57704c4d6`

```dockerfile
```

-	Layers:
	-	`sha256:3c9a923b78416ca066aef3ab1d878eea27faca6457bd26d1bf5f90339a0a7e34`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 3.1 MB (3148151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0bc7cca002a27ab772491a21bf4c0b3e84939fb73196d6ab16aaeddcf5c93e`  
		Last Modified: Tue, 03 Feb 2026 02:16:09 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:781c3f7b8be50b770eb85935183eb92da8bb31ec4afb9b55d4f0c0e7a8a55310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53582889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa312940c5314679a39349b200e9c2e94ef8a0302aebc9a000f441696d7cc1ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:14:18 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a0a026d4bb771de47d622d680861a5062bd4e0c02e6c2d817a503a12b7411ab`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 53.6 MB (53582665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38fcfc8e009a023f698b2aaa5bda6c2ceb68bbe28c22cdc1b959ecde4ebec17`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1274ee74c1229040a686d23f86e3fac94808ddb06b80a182f5ae9596d4556b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bb6b9bb768f85ebc40c30fa67b3f09337271e0bb4cdbdcd34ef2b73ede9ef`

```dockerfile
```

-	Layers:
	-	`sha256:633145368ce55ba0b37071e3eb674781bd186016d0d1a1c74b84445452e66f47`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 3.2 MB (3154480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45cf4f76e10dd3ad18ae6ed336ef32bf9089ea00c8824e6da22dd888869f1c3`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:f451d4695b411f9102ce34de3118930d66c2dc0b6b585df75c9f3792dbf177c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46854686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557810dfa53da63142a437854fe76ad2fc9597a3761e48249c9f83f293c820d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1768176000'
# Wed, 14 Jan 2026 04:03:34 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0d152d1dcac9b1a7bbc763f3f2f3b2328b12317f387036c0ef1af1b70d3cf327`  
		Last Modified: Tue, 13 Jan 2026 00:52:30 GMT  
		Size: 46.9 MB (46854463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0f696d74d96ec399c468956e1ee94f1fa01dfc59dd3a9f02df83a04f80a517`  
		Last Modified: Wed, 14 Jan 2026 04:04:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fa95fde284364994b8e58f824b53d6c139c212aaaf427800c8c610b463ee438e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06840bac843257cae22e73e27707d99e409029cb194d87fa6f3dca8b74ecf218`

```dockerfile
```

-	Layers:
	-	`sha256:225c4abc6dc48755ab71b9d3b7fa664457807c2e131a22a6f9daad91be15f269`  
		Last Modified: Wed, 14 Jan 2026 04:04:29 GMT  
		Size: 3.1 MB (3133537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d81530a876e6438436c53ebfe68ecf92a6e6da9c189eb58576a3afa74b0cdf`  
		Last Modified: Wed, 14 Jan 2026 04:04:28 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:916753e7eac3becf7bd138bb94a571920ad9ef1b22622cda5c99c6e9ee1f8157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48429556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db09a64cabd952b41d70edac9791a252ddd9474c69bc07f0f292903dca68d411`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:15:15 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:616d765aba14d266e800a78cc4d0cdbfd95c5d967a141135b80d41a64ad5ee62`  
		Last Modified: Tue, 03 Feb 2026 01:12:49 GMT  
		Size: 48.4 MB (48429330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b5be8a80213d43e0a1d74dd392d7086e53f87094dc9abe2ad57b956313d9d2`  
		Last Modified: Tue, 03 Feb 2026 02:15:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8d9dd74c50ef601c0b0b5a040be1201a5ba7094d9c1f1e6e430050b517c9e6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d809fc362ccd8e1a1bb386ca97dc9a2fecf0dbbe9439e8752f216fc44d46db`

```dockerfile
```

-	Layers:
	-	`sha256:625f896e07f2ebf4a1d2e34e46736549c162537c71d8333ff56eff5145e7af8f`  
		Last Modified: Tue, 03 Feb 2026 02:15:26 GMT  
		Size: 3.2 MB (3152406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fda7e0edf35888deab71d955111577572a872cd1ea8bd33471f1d5bc3735e7a`  
		Last Modified: Tue, 03 Feb 2026 02:15:26 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
