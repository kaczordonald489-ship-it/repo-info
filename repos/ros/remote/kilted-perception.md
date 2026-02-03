## `ros:kilted-perception`

```console
$ docker pull ros@sha256:8e4eee6ee425b167586bc2e29348cc0e49989c08d709297bc0acb301bc9b7add
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:524fcedea8e3843f148921b4d17564acebbcceb1b24f1d003aa12c3f1348746f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081910838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a3859b578b4c88e9985084d8d8a179f0bf0ac21a7990c76b22d98258ce8086`
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
# Thu, 15 Jan 2026 22:40:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:41:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:36 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:24:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fae7f48a46da951e313f18a6daf495d637bd45e1d4f7d040911c1f2ee7b972`  
		Last Modified: Thu, 15 Jan 2026 22:42:02 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc1c27f9559dd6ff1cdbfe218890a4794f42a6099b771506e057d7764a7720`  
		Last Modified: Thu, 15 Jan 2026 22:42:02 GMT  
		Size: 6.7 MB (6747522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21f7fe8d5212d488b694908db57f4df8b1edd9165e7ef82d3b595cb236521`  
		Last Modified: Thu, 15 Jan 2026 22:42:02 GMT  
		Size: 94.2 KB (94176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b77d824f0ae70e13124dcbd7bfd2d9fac9328ca8a3a90e3f5993a9b4afe030`  
		Last Modified: Thu, 15 Jan 2026 22:42:05 GMT  
		Size: 121.0 MB (121016025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206cf29389588b7b19b55414eb210e1dd6f08621c5925cc97783e2512e2448b`  
		Last Modified: Thu, 15 Jan 2026 22:42:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139627acf1d2dfacd85fc36c6189af287834fafc74629ff2615296c058bf3da`  
		Last Modified: Fri, 16 Jan 2026 00:58:44 GMT  
		Size: 110.2 MB (110187099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e2efff092f53ee7789ee08cbb160b3b85b87524a06744e8e91cab9cf9ca171`  
		Last Modified: Fri, 16 Jan 2026 00:58:41 GMT  
		Size: 371.7 KB (371744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723794c7050a1b79f891d804f844d9e39317679cba5ca2031f687bca2592df7b`  
		Last Modified: Fri, 16 Jan 2026 00:58:41 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06850daf351b3a2227558f1f02fa276838ebc17e954b4895c983ca9efa734cbb`  
		Last Modified: Fri, 16 Jan 2026 00:58:42 GMT  
		Size: 28.1 MB (28063475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44509b06494e9ebddb82569eccb862b387e470f2a3453e492434d080a51c6b7f`  
		Last Modified: Fri, 16 Jan 2026 02:27:18 GMT  
		Size: 785.0 MB (785018077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:977ea51a176211c26eef3a00a1317d4537bc50586f5904af962a1d81d2bed622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60765898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e6fefdd3bc9d1b2799aaaf2859d8b103327f5ca9d406220bed245649156a8b`

```dockerfile
```

-	Layers:
	-	`sha256:51c35517fcc146840add078a61b6c28bab018fd2ee9d2a3a519617a275ce42d6`  
		Last Modified: Fri, 16 Jan 2026 02:27:05 GMT  
		Size: 60.8 MB (60756546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:614aa670fbc9747282c6123f07032afe79b0f9bede547041178994e20bc54a0a`  
		Last Modified: Fri, 16 Jan 2026 02:27:02 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd4c4bbb02d1c6d9889dd6995bb0f1319a518f2efc2a4c4e1cf3a04502efd557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.3 MB (980330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a6147ff544709189290ba0a49dc5a77d96fbc153620cf0cf4aa26be812508e`
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
# Thu, 15 Jan 2026 22:43:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:41 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:44:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:24 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0ffeb8abf9f69d9152d9ddf05b3d9bf0abd0da07487f555fca9183c211600`  
		Last Modified: Thu, 15 Jan 2026 22:44:52 GMT  
		Size: 684.1 KB (684101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec456ec14866e45cf8752da07321782d64ae4e50014222025f952c73348f74`  
		Last Modified: Thu, 15 Jan 2026 22:44:53 GMT  
		Size: 6.8 MB (6761200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535702c99d332d44232b15396c6984e051db229f065200199d57a426a3e62760`  
		Last Modified: Thu, 15 Jan 2026 22:44:52 GMT  
		Size: 94.3 KB (94254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41213d7b9319bb10daf024007dce1857fe9d550536f830b9d1d7646b1c9007`  
		Last Modified: Thu, 15 Jan 2026 22:44:56 GMT  
		Size: 115.7 MB (115742618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee8712744d000fd48a2c882b325511146d3667fa87b4546ad01002eb3efcd4`  
		Last Modified: Thu, 15 Jan 2026 22:44:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fe46905465de7cdf7df0c256bc882a5c6f6bce00a12443b384513c5446e4ec`  
		Last Modified: Fri, 16 Jan 2026 01:01:56 GMT  
		Size: 105.6 MB (105595239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09271007bf03040fc00ce410c5798e4c25d9a95699468661d096af654f19d170`  
		Last Modified: Fri, 16 Jan 2026 01:01:53 GMT  
		Size: 371.7 KB (371749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53da40f77632a2aede7a153c740aa61a40ad8c211cd72001665ddd01a1f91a58`  
		Last Modified: Fri, 16 Jan 2026 01:01:53 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf3e21264a6cf710a3de027e72eb48ed241babcb1b8c1ba3d0457d768260a11`  
		Last Modified: Fri, 16 Jan 2026 01:01:54 GMT  
		Size: 27.1 MB (27144525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5b0320544a6cb0be947c4f507340bd9c19d88ce26bc7229a7085a522f1c066`  
		Last Modified: Fri, 16 Jan 2026 02:42:18 GMT  
		Size: 695.1 MB (695069904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0570c4e60ad2753417303f2b32e0af0f94eefe99b015a00a3f36bee4ac22661f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60696503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ad0f9a8716c33686e3efe62ff3c85043b705344c16896eefa11fcc76eeeaea`

```dockerfile
```

-	Layers:
	-	`sha256:6722119cc6218fe2cc328fbf7d2db24be8a4cb3a120a96133e4512cbd4af06f7`  
		Last Modified: Fri, 16 Jan 2026 02:42:06 GMT  
		Size: 60.7 MB (60687071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424387a98a10ea1326380f6cb894dc7d38536fad36fdd3fc25554e9c625b9578`  
		Last Modified: Fri, 16 Jan 2026 02:42:03 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
