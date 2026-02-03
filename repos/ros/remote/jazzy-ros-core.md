## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:71b21e1390c09b35f73999111c61b7fe75d51bb4a5217d27a4bdd72fa9e21ca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d22508ec16651e1719c347630de078a2627d97667d60f9efeb91271298e7e4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157472885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc26263419dba1dbf419e1eb7c55c3033836cdc79171cf4c24d2f1f11f3b544`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:31 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:31 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:31 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:34 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:718bacb15f35078b0f28d8b6047d5c326fe40fe47fd37142e7b8512656dbcdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c07be828c2fac7a05fbe19e8c0d476f19a510ed25c4e30c61b9941793b847b6`

```dockerfile
```

-	Layers:
	-	`sha256:6dca5a67023b62c342e40a64f5d0717f56e26a2eb18cc49dd99ee95a1d8b9248`  
		Last Modified: Thu, 15 Jan 2026 22:41:32 GMT  
		Size: 18.3 MB (18301254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d33a19228a0f7b7e5affac08b64dd7b3018d9918f08433340ad526703e3352b`  
		Last Modified: Thu, 15 Jan 2026 22:41:31 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25f346d4dbf19305ea83113abb49583cb9327ec9c001a11028a62a8bc046ec5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151397228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98868b6a2a3d210a3b8da7ba7f82445bc7c98c3122feca22287a21dd940849b7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:30 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:30 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:30 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:33 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:244624508e6ef55aaeba85735fa4607485b5b4edef248eab60e6a551218e88c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981da7bd5f5fa9436399bdfe216f1a2714f1211b91630059a9109f1d3f89c5a`

```dockerfile
```

-	Layers:
	-	`sha256:9337bd5620a9882a694b82a266e8d2edd29bfbdbf6693e5ae60367f41a2407be`  
		Last Modified: Thu, 15 Jan 2026 22:44:31 GMT  
		Size: 18.3 MB (18275260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6852199e7efbbfe0640b063a1e2afe61733440d39d665644169a40f486ca6e8`  
		Last Modified: Thu, 15 Jan 2026 22:44:30 GMT  
		Size: 14.7 KB (14724 bytes)  
		MIME: application/vnd.in-toto+json
