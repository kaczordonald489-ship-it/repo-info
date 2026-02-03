## `ros:humble-perception`

```console
$ docker pull ros@sha256:36f93aeb176121a456dc52cd9f98de940b5d1f7fd73730666cc65208332110ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:c9266fe808f8b9030dace34a2ebc33e9b9e84e9af292aec95790945968f99006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.3 MB (955283169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08bd40e585234468cb47ef6d41b2291bd8c8d43142d22b3041733649dbf07d9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:50 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:56:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:56:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:56:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:56:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:18:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f147c465ef3441f6a6fadaa4bf3dd1b68d753988b404893e8e575a24a013be1`  
		Last Modified: Thu, 15 Jan 2026 22:41:15 GMT  
		Size: 1.2 MB (1214139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b6a798b5088fee7bc0bfb188bdd445113b407842d17edf502e09f2fc1b536`  
		Last Modified: Thu, 15 Jan 2026 22:41:16 GMT  
		Size: 6.0 MB (5992568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd839ce83db999d5035a7a3825b0dfa72a58cb764b8a8ea0c500fbed89b583b`  
		Last Modified: Thu, 15 Jan 2026 22:41:15 GMT  
		Size: 97.2 KB (97222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e1824e50f15537f4e31add7722621bc890f927e27f1505e54da0b51bc4c1b`  
		Last Modified: Thu, 15 Jan 2026 22:41:19 GMT  
		Size: 104.7 MB (104703723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dabda1f44ba2f0c461142f451ba75451f7348aa265fbe6a04dd0ff2654448d`  
		Last Modified: Thu, 15 Jan 2026 22:41:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aaf05f7e4717206bdef277969fefae295f0aeb84ad86377ce147c6e467ce29`  
		Last Modified: Fri, 16 Jan 2026 00:57:31 GMT  
		Size: 98.0 MB (97958403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e9ae4043d817eb2f5f8b33584b61dd9859d8733be7d8c069ae9efe648e3d28`  
		Last Modified: Fri, 16 Jan 2026 00:57:28 GMT  
		Size: 383.1 KB (383080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c9c540e89d0a29bced540968ac923c8677aab6a43d85b536f173a4e668d7a7`  
		Last Modified: Fri, 16 Jan 2026 00:57:28 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89d0b0792ec60ed6744e3a288f76caa6009884e44c6cd98add8055465bd325c`  
		Last Modified: Fri, 16 Jan 2026 00:57:29 GMT  
		Size: 23.3 MB (23319499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023ff6a287f1eb5573aa2080be2d3b1cd2777a0402ca0353ddd4391113d164e2`  
		Last Modified: Fri, 16 Jan 2026 02:21:33 GMT  
		Size: 692.1 MB (692075143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:14526acefc3ca7b2dce95b9c304572c829a1be3e0ca71840580b52b5e755c2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58802650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a8447206951ee8cf85719d2eaf0d00a2e58c754ecce8523ec6503759e84378`

```dockerfile
```

-	Layers:
	-	`sha256:ad10d14853e9a536ef154ad654f2292b9fbc6ad69306ad73ae2ebe46755cc01b`  
		Last Modified: Fri, 16 Jan 2026 02:21:21 GMT  
		Size: 58.8 MB (58793298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8fef5d048b424b40e20b36d98c0d5c5f6309fc9f8d7d2a284d32369d1c64a5`  
		Last Modified: Fri, 16 Jan 2026 02:21:19 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:60f176c5d21213851d242397d36fbd4f5678d97d748807c23bb1639f6525c3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.8 MB (915843147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b64736599a00eaabcfed647981112798414920e60c26eacb402d2adc8dabd08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:42:04 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:59:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:59:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:59:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:38:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4eaed05c1178f3c3abdac8710778abf118d80e3bc2740ff1270b8e4316b14`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 1.2 MB (1214255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8fdf13cb39747e8c67471f5fd7e7eb6060b2cf311a7e56c64f6ea8a77a5b63`  
		Last Modified: Thu, 15 Jan 2026 22:42:31 GMT  
		Size: 5.9 MB (5943245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e54e499a91704d69c814930daaf58f6daab8d4e90cb5515d9292d6adf0420`  
		Last Modified: Thu, 15 Jan 2026 22:42:30 GMT  
		Size: 97.3 KB (97262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01a8729ed4ffcbfea0a8f2b6e3d75fb2b3d6fbca0adae54bdcca438384f878`  
		Last Modified: Thu, 15 Jan 2026 22:42:33 GMT  
		Size: 102.5 MB (102461954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb96ce313cf0c46ab959a2078235f16180a94cb84463bf95ee21b57ddee0bd9`  
		Last Modified: Thu, 15 Jan 2026 22:42:32 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a9f60ba1df891822ce0d8130763f31a13c443b9ebfe1c0e440fcd3e6c191f`  
		Last Modified: Fri, 16 Jan 2026 01:00:46 GMT  
		Size: 95.6 MB (95570423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1972aab6a9eb97320567f599408f1b3c042d45b4d5cf98a47df3fae37d322ba5`  
		Last Modified: Fri, 16 Jan 2026 01:00:44 GMT  
		Size: 383.1 KB (383089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7bad824db54a24fe8e28696df6152c09a70dad3ed062036f227f5166cdcf`  
		Last Modified: Fri, 16 Jan 2026 01:00:43 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7449e37e4f9d95d850d1345d99e92afc5b1075877cd1809b099c884e46a26eb8`  
		Last Modified: Fri, 16 Jan 2026 01:00:45 GMT  
		Size: 22.7 MB (22718477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0071f0e10683b12f6b212343cd3ddf97112454c4a0682fb494803a32937e43d9`  
		Last Modified: Fri, 16 Jan 2026 02:41:40 GMT  
		Size: 660.1 MB (660068251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:41cddc50b1f93e042b42d1f5caf5a546438723963d5795beb650a5ad31cf43aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58787050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a4dc2f79e44e2a7b9b339376503328e7bd1f289b87a17f44fed2b8e8c5d67d`

```dockerfile
```

-	Layers:
	-	`sha256:7bd792af3432cac3a0b2d5c1cb50f81502492d4b6097a63238c83cf7ef4e35d0`  
		Last Modified: Fri, 16 Jan 2026 02:41:29 GMT  
		Size: 58.8 MB (58777619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e915bb7e5c8e07c0bc13c8e8d9155aa9e54bbfc18fc3266ac8f99f945ff92ff6`  
		Last Modified: Fri, 16 Jan 2026 02:41:27 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json
