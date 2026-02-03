## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:e9868b11c447ebe7d96de318281652fbde5f881a6d918037363772cb216ebb45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0358858d92326a489fc804735ed5ca3234bbac05b9287990d76c46a259f52041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324895138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89545a1401c5c5dd27da58db684417a8589ac75a6930ed52790d743fd3d19294`
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
# Thu, 15 Jan 2026 22:40:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:41:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:59 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:58:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:58:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967b3bea28a190de2abdf7c583b9e2b113486381b15ce00e1bb91c9c58c7026`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 684.0 KB (684002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e126b2b2995cf775c0d4c7132e48cc59964feb7907083276ec56e4887393982`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 6.7 MB (6747551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18b8569b1a8cc779459c80d4f6fe5de9295d36844ee1136e7c0f679a38d436`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 94.2 KB (94195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81824252ed26645e4cda94990da14222e41928058bbb7b3049257c78f69ab5ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:35 GMT  
		Size: 149.3 MB (149258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af2ca8fd7a12110b28f79aec36ece2ed6d1deb02337ced830f83efc91a62c`  
		Last Modified: Thu, 15 Jan 2026 22:42:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f49599d4013baaab168de3657e56f1a064b0c2b3905abef079ce53580b55fc`  
		Last Modified: Fri, 16 Jan 2026 00:59:38 GMT  
		Size: 110.2 MB (110187905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803c8199c566f7183c9af620273eaa14079f91449307d2f85488be3e5b8e31c`  
		Last Modified: Fri, 16 Jan 2026 00:59:34 GMT  
		Size: 364.1 KB (364083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6037797cc4818e4cb6c652d9119165eb136a640dc847c7a40b2a255d82140d78`  
		Last Modified: Fri, 16 Jan 2026 00:59:34 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6e075818bb92799b42233693868bc52253c0460cd5c0e34ea859c07eb2f032`  
		Last Modified: Fri, 16 Jan 2026 00:59:36 GMT  
		Size: 27.8 MB (27830020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0909ce67644b3bab13463a71aa6f9e981e2e187022e60ef9b8cbaaad03935a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25699011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b916b8e46b524b26de20e043f4e2fed111ddefdfe51bc3db56e9dac335205b78`

```dockerfile
```

-	Layers:
	-	`sha256:9ecceda629293cd8071874563df336cee41e97acbb6142fd065e37ac09144a77`  
		Last Modified: Fri, 16 Jan 2026 00:59:35 GMT  
		Size: 25.7 MB (25682647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3d376c3c92ce9b464afe89b4cfb7c629da8bf85fca826b6be3f88a5b7f6e93`  
		Last Modified: Fri, 16 Jan 2026 00:59:34 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81c71294829ca2f68c2f5dccb482e2ad86989f10e297a710c8e98d5408bce385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312875893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8292860f47d9ade8e2fdc86cb4b23a6c2cfd586e6d0dda17874d9297a0ebde02`
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
# Thu, 15 Jan 2026 22:43:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:58 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:01:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7bce41f2844e04d79191a3a4c295cceebd907050fdd985904094c9ba0d985`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e13d723b56be5d113451d0159f2a683e7ddac92cc7b441e356a56355ff611f`  
		Last Modified: Thu, 15 Jan 2026 22:45:15 GMT  
		Size: 6.8 MB (6761189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897c68b882e54cfb023792aa6fe744ee9e750aa8568087884c4fb4ab09101ad`  
		Last Modified: Thu, 15 Jan 2026 22:45:15 GMT  
		Size: 94.3 KB (94257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36529be7c1d16a05a9345b5d7fe602935226342c7f00f326043ca6356711d8b3`  
		Last Modified: Thu, 15 Jan 2026 22:45:19 GMT  
		Size: 143.6 MB (143598736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca3447fca213716c45fecc334db425ccb842ed9d7e99dadaea901c500b2d79`  
		Last Modified: Thu, 15 Jan 2026 22:45:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d0315754ad467c0f84a51bcca420f9d00efc89dd6b14a66ca9b67d15cc1515`  
		Last Modified: Fri, 16 Jan 2026 01:02:36 GMT  
		Size: 105.6 MB (105595993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d98324865d792dbec7fdb6bca34a68a242ff693752ea91e79792218d79eb584`  
		Last Modified: Fri, 16 Jan 2026 01:02:33 GMT  
		Size: 364.1 KB (364075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90a40e53a65c744875af2e18cbb0eaa9054b3b722a5cbb8ead531fbd150be6f`  
		Last Modified: Fri, 16 Jan 2026 01:02:33 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63502b76303910712c34ce860754310acbc8ecacdb2103d23eda093422cc82fe`  
		Last Modified: Fri, 16 Jan 2026 01:02:34 GMT  
		Size: 26.9 MB (26911011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a1b5bd7b8e9c69f87b63f3bc6027af2740dcb73babc868272daac09819f37b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25721607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e66317b9ddc7c9918532d1125d277207524e7577c41b1d90645ad7f420af9b`

```dockerfile
```

-	Layers:
	-	`sha256:20a29c1b578495a9aa8a2c361c2c383a0002adb9930920daf6b6f9a6fafeb7f8`  
		Last Modified: Fri, 16 Jan 2026 01:02:34 GMT  
		Size: 25.7 MB (25705105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa5771aa61e4f4274fac2fc7d47a1d3a13b759c62a1d445d2b443c06b14acf`  
		Last Modified: Fri, 16 Jan 2026 01:02:33 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
