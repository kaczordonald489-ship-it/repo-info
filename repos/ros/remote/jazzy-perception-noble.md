## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:07592661fad906f43ee695724005e582ba4ff7091c0e6a0c90368a783d28f6f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:2a12f903dc4255a2c257402998cfcce0bbb489e0fae56045b2d8ad3c55bd7293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080595938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3973d7319306a198fd47dc52345b0077ae0976903622b204edca944271fda958`
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
# Fri, 16 Jan 2026 00:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:57:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:18:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:51a2d5b61aaf7e2e0547a70431b18a46188a6e920efa30a196e73b6b9abd45f4`  
		Last Modified: Fri, 16 Jan 2026 00:58:11 GMT  
		Size: 110.2 MB (110183100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758dc4c4511d77e8139294b47787d28096781d5b2ef8f4caf1144e9fbe6f561`  
		Last Modified: Fri, 16 Jan 2026 00:58:07 GMT  
		Size: 390.3 KB (390326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda5a314ef599a1d2f9db599331d5bf2e05dc8c9b658de57954f6a5f24d246ad`  
		Last Modified: Fri, 16 Jan 2026 00:58:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673747666502f74a4c28e3b441004032e9d058d9b70a031ca3606ea0644f87b3`  
		Last Modified: Fri, 16 Jan 2026 00:58:09 GMT  
		Size: 28.0 MB (28005148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879fd0bc64f670b143d1fb667f9b7e233ea4fe0052e831f9980cb7ce9dccb594`  
		Last Modified: Fri, 16 Jan 2026 02:22:17 GMT  
		Size: 784.5 MB (784541975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9069d0dc9e162fe61158ecf2e6ab7963ed9ccf6a83df07a98a823fca4e8dd700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714d78dcce09f7a48c64365aa9c386dfa8420b1c1bd5567a6f9646d6ab07a219`

```dockerfile
```

-	Layers:
	-	`sha256:c0c8cb106ae1995803c4231e75112969d382d2aa99fb6ab3f64ca4e8847b4f8c`  
		Last Modified: Fri, 16 Jan 2026 02:22:04 GMT  
		Size: 60.7 MB (60706642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5736688820fda8cfbc8f92610ddf2bd848765d3d7a7c8c7246dcd2f9fb3ac8`  
		Last Modified: Fri, 16 Jan 2026 02:22:01 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fb966efe4b8c82781a49ac2979f9c65606d60f3443f70184d3b93a39e3200e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.0 MB (979006040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bb2927dad395a6964a942fd71515971cac60ec75b4c840eaf790596d423aa1`
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
# Fri, 16 Jan 2026 01:00:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:00:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:00:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:39:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:82ded0d19c79a23e1eb3c9c493b71bc3aaf47b095d79cdf0da647eb55203289a`  
		Last Modified: Fri, 16 Jan 2026 01:01:25 GMT  
		Size: 105.6 MB (105592399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a29344c731ff62579c4b41928a004f7229c263244eb3cf2e9cfa02ee6a82911`  
		Last Modified: Fri, 16 Jan 2026 01:01:22 GMT  
		Size: 390.3 KB (390338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdb3e21e95af01abb665679711c101cb346091241dab45013bb305b86c3f28`  
		Last Modified: Fri, 16 Jan 2026 01:01:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215247acb520778e621dccad3a665d57a8e8bd9d18e532c921fde7b876b7e46`  
		Last Modified: Fri, 16 Jan 2026 01:01:24 GMT  
		Size: 27.1 MB (27099655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7700dcd0492c8b111be48629f1f7ad575f433a8e6a8a8b7668d43f94a63f0f59`  
		Last Modified: Fri, 16 Jan 2026 02:42:21 GMT  
		Size: 694.5 MB (694523908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:008d08adbc88f612293f059db9604d85c2349d837a72d7048f8ab4fcd9b7a939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60646585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302f3aa562975ff6cca0b263931cb561ac8b8919bd7673807fae4f1298302be4`

```dockerfile
```

-	Layers:
	-	`sha256:16ea6dd4ccb3f236a1260f5b0dd2bd65681ca0ebd9e1277ece5689c5cfc3c67f`  
		Last Modified: Fri, 16 Jan 2026 02:42:10 GMT  
		Size: 60.6 MB (60637167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c567016c443d1d8718e754ea8c22d8483cf16ae661dfd30cf0639e16b7235c2`  
		Last Modified: Fri, 16 Jan 2026 02:42:07 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.in-toto+json
