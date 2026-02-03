## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:4e0197b33afe3a4f6e881e1478d79fa9b374a8e2a155209678eba09d53ad460d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:9e0739f8d0c7b66dd78c61853d0f8d3803c53bff95f8384226a061556cf81784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296892761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cad5147080770cde20dab3d15b86eb33c5ba126674235c2f4fbfa73957ca86`
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

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:88c7a9fb1d1e64d01df3cf05229a4b9c9e803860bcfa123bc4958b6720acfe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24600251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66db517cc6a7ebecdab82a2812cf460be1665864b80237f96fe73da203108045`

```dockerfile
```

-	Layers:
	-	`sha256:f0459c0d1e93f372bc00f9de10850f232cac56d0bdd746a4ac7b794e60636578`  
		Last Modified: Fri, 16 Jan 2026 00:58:42 GMT  
		Size: 24.6 MB (24583904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814a4b4c3e95a6478b13dfc14eb736461afc47c6f7070915ccc6b04b85762a95`  
		Last Modified: Fri, 16 Jan 2026 00:58:41 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d40086d2c2c1539b1a8eee67e35a0d1cd7104a23813a8bfc2098d7323f14581c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285260217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f27d37d0626e98ab374aad076c6fc617065002dc2aa185faaf91f22385b9f`
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

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a488e8c6562c5bf506883d9347416992ef055c6c2882ab8215a6c78a25ca4f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24622649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cdb796ffdafb23da6b45ed06f8bf1fef5d600da824ab8d268824b74ad35f59`

```dockerfile
```

-	Layers:
	-	`sha256:42ea77cedb88eb06075335c1896ee3a19f0b13156db6a51af9f9153d82234249`  
		Last Modified: Fri, 16 Jan 2026 01:01:54 GMT  
		Size: 24.6 MB (24606165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cac50e00f17e0383ef1f9fe799d22b586da1fbc5372c1220ef1e3bcc7142dc9`  
		Last Modified: Fri, 16 Jan 2026 01:01:53 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json
