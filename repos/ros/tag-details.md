<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:kilted`](#roskilted)
-	[`ros:kilted-perception`](#roskilted-perception)
-	[`ros:kilted-perception-noble`](#roskilted-perception-noble)
-	[`ros:kilted-ros-base`](#roskilted-ros-base)
-	[`ros:kilted-ros-base-noble`](#roskilted-ros-base-noble)
-	[`ros:kilted-ros-core`](#roskilted-ros-core)
-	[`ros:kilted-ros-core-noble`](#roskilted-ros-core-noble)
-	[`ros:latest`](#roslatest)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:370191995451bb63f2e37bb2f6636a09f66ca810d0865703058361dc6ac70c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:50ca1476252d8fe40674d7dea071c26fb42150aa2caeb802d8c28eebb4e7eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263188860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5ee94de7e3852df5106a42cfeab65f5ab15d194963accc6886e8641cc08a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:6d5170a3809927780690b6aa99b24993fe9d338800198d4b8bf4c9dc84bb9598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770354243fc7649f5cb1beb98b9a2f7e0668df502b493957f0d1ce6acc9ea75`

```dockerfile
```

-	Layers:
	-	`sha256:b46162c66a49438be9b0ca0afc097ed4b1ead8c95b9953ed9fc1b7088211f252`  
		Last Modified: Fri, 14 Nov 2025 02:17:47 GMT  
		Size: 23.7 MB (23678894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a59713e8a6d17917071f2a700a2b1634fab032b25eddc10b2b25a98a95f45`  
		Last Modified: Fri, 14 Nov 2025 02:17:48 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eea6e5a39edbbb606c3ab6a9755da16b0164b38883bd56f39ebf3268841960bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e63ae3b688e64872daf5a5e363a67e43249ef25fc4da49c363aec409953cd64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:292b8380d247e9ac7d575be970a46b0a90e4568fa92841ebd697d87c1240d9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23708396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922522fecc436cb20f7040b0227e8dc8c46b5f9ac9981d9425fb52d2ab0d397`

```dockerfile
```

-	Layers:
	-	`sha256:6f10a08a03a11cd3796fdc3b6159f068cf58a7b55c4910257a8d3300f71e55e9`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 23.7 MB (23691911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb23ec2ff4e9d03fd8af8d8d1f01c4a5c73fdbd14991061c2dd3fac91a32092c`  
		Last Modified: Fri, 14 Nov 2025 02:18:09 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:f14906d4a3ca82fa13ec7f8c79d237a04f6a14d47b69564f25eac6903d319d91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:4e413449e965df0365d69f8c3d1ba8cfcce7462055b2e9f553946038c8fb889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.3 MB (955267423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59770bcd3cb81de41bcfcb45df3b1cd13f144652a4103b9c8a561013c176d044`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0d0741124ce4b0fb32492f0eb411c68db26f35feb0021f90eb30e7d54f867`  
		Last Modified: Fri, 14 Nov 2025 05:35:32 GMT  
		Size: 692.1 MB (692078563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:beb8f658a1af83eb45d4c219d7a6dddd8461f1e6b5ea407917e43aa8cd78d417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58779844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b398c9069f37afa0b64dea4ee59863980189e9bd72350262c9e4f2856040857`

```dockerfile
```

-	Layers:
	-	`sha256:3c05b9e971b9f7a4606bc635dfdf55c3ac7a74cf9a4f7f7b93590ddc2e8daf03`  
		Last Modified: Fri, 14 Nov 2025 05:17:41 GMT  
		Size: 58.8 MB (58770492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a507faa299531991695a31b8854ae95bdd28604e7ac848e2dde9065c3bedf8f9`  
		Last Modified: Fri, 14 Nov 2025 05:17:43 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec183011cf6e60839ceb21854426cef343bcef506019abed261c30357f959409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.8 MB (915797607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9d2f3550dab7e144828cc7546b305d487aa457c6f459bffdc4c1036ff187f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11e17f04355c02a9eadea3e0924ee22951e0a76af18b90e7a44e2cfada4c52`  
		Last Modified: Fri, 14 Nov 2025 05:31:54 GMT  
		Size: 660.1 MB (660050278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:20b8cc1b1082051f1c1937e4002197a0acdd8ee796f9d9b17dd686ade332e9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58764245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215b91a017e92d95162e756c7abc222791ac87f692ccc607510a10866c6f48b`

```dockerfile
```

-	Layers:
	-	`sha256:6e41f5d137270010cee9c967c7b1f18ec19e7de3cbe729d862fed5b6a2859920`  
		Last Modified: Fri, 14 Nov 2025 05:19:30 GMT  
		Size: 58.8 MB (58754813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0b1e8fd8dd6d89eda990d19a48a4735fd6141dee4434e2b642439d6a90f13e`  
		Last Modified: Fri, 14 Nov 2025 05:19:32 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:f14906d4a3ca82fa13ec7f8c79d237a04f6a14d47b69564f25eac6903d319d91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:4e413449e965df0365d69f8c3d1ba8cfcce7462055b2e9f553946038c8fb889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.3 MB (955267423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59770bcd3cb81de41bcfcb45df3b1cd13f144652a4103b9c8a561013c176d044`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0d0741124ce4b0fb32492f0eb411c68db26f35feb0021f90eb30e7d54f867`  
		Last Modified: Fri, 14 Nov 2025 05:35:32 GMT  
		Size: 692.1 MB (692078563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:beb8f658a1af83eb45d4c219d7a6dddd8461f1e6b5ea407917e43aa8cd78d417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58779844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b398c9069f37afa0b64dea4ee59863980189e9bd72350262c9e4f2856040857`

```dockerfile
```

-	Layers:
	-	`sha256:3c05b9e971b9f7a4606bc635dfdf55c3ac7a74cf9a4f7f7b93590ddc2e8daf03`  
		Last Modified: Fri, 14 Nov 2025 05:17:41 GMT  
		Size: 58.8 MB (58770492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a507faa299531991695a31b8854ae95bdd28604e7ac848e2dde9065c3bedf8f9`  
		Last Modified: Fri, 14 Nov 2025 05:17:43 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec183011cf6e60839ceb21854426cef343bcef506019abed261c30357f959409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.8 MB (915797607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9d2f3550dab7e144828cc7546b305d487aa457c6f459bffdc4c1036ff187f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11e17f04355c02a9eadea3e0924ee22951e0a76af18b90e7a44e2cfada4c52`  
		Last Modified: Fri, 14 Nov 2025 05:31:54 GMT  
		Size: 660.1 MB (660050278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:20b8cc1b1082051f1c1937e4002197a0acdd8ee796f9d9b17dd686ade332e9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58764245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215b91a017e92d95162e756c7abc222791ac87f692ccc607510a10866c6f48b`

```dockerfile
```

-	Layers:
	-	`sha256:6e41f5d137270010cee9c967c7b1f18ec19e7de3cbe729d862fed5b6a2859920`  
		Last Modified: Fri, 14 Nov 2025 05:19:30 GMT  
		Size: 58.8 MB (58754813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0b1e8fd8dd6d89eda990d19a48a4735fd6141dee4434e2b642439d6a90f13e`  
		Last Modified: Fri, 14 Nov 2025 05:19:32 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:370191995451bb63f2e37bb2f6636a09f66ca810d0865703058361dc6ac70c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:50ca1476252d8fe40674d7dea071c26fb42150aa2caeb802d8c28eebb4e7eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263188860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5ee94de7e3852df5106a42cfeab65f5ab15d194963accc6886e8641cc08a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6d5170a3809927780690b6aa99b24993fe9d338800198d4b8bf4c9dc84bb9598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770354243fc7649f5cb1beb98b9a2f7e0668df502b493957f0d1ce6acc9ea75`

```dockerfile
```

-	Layers:
	-	`sha256:b46162c66a49438be9b0ca0afc097ed4b1ead8c95b9953ed9fc1b7088211f252`  
		Last Modified: Fri, 14 Nov 2025 02:17:47 GMT  
		Size: 23.7 MB (23678894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a59713e8a6d17917071f2a700a2b1634fab032b25eddc10b2b25a98a95f45`  
		Last Modified: Fri, 14 Nov 2025 02:17:48 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eea6e5a39edbbb606c3ab6a9755da16b0164b38883bd56f39ebf3268841960bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e63ae3b688e64872daf5a5e363a67e43249ef25fc4da49c363aec409953cd64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:292b8380d247e9ac7d575be970a46b0a90e4568fa92841ebd697d87c1240d9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23708396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922522fecc436cb20f7040b0227e8dc8c46b5f9ac9981d9425fb52d2ab0d397`

```dockerfile
```

-	Layers:
	-	`sha256:6f10a08a03a11cd3796fdc3b6159f068cf58a7b55c4910257a8d3300f71e55e9`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 23.7 MB (23691911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb23ec2ff4e9d03fd8af8d8d1f01c4a5c73fdbd14991061c2dd3fac91a32092c`  
		Last Modified: Fri, 14 Nov 2025 02:18:09 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:370191995451bb63f2e37bb2f6636a09f66ca810d0865703058361dc6ac70c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:50ca1476252d8fe40674d7dea071c26fb42150aa2caeb802d8c28eebb4e7eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263188860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5ee94de7e3852df5106a42cfeab65f5ab15d194963accc6886e8641cc08a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:6d5170a3809927780690b6aa99b24993fe9d338800198d4b8bf4c9dc84bb9598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770354243fc7649f5cb1beb98b9a2f7e0668df502b493957f0d1ce6acc9ea75`

```dockerfile
```

-	Layers:
	-	`sha256:b46162c66a49438be9b0ca0afc097ed4b1ead8c95b9953ed9fc1b7088211f252`  
		Last Modified: Fri, 14 Nov 2025 02:17:47 GMT  
		Size: 23.7 MB (23678894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a59713e8a6d17917071f2a700a2b1634fab032b25eddc10b2b25a98a95f45`  
		Last Modified: Fri, 14 Nov 2025 02:17:48 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eea6e5a39edbbb606c3ab6a9755da16b0164b38883bd56f39ebf3268841960bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e63ae3b688e64872daf5a5e363a67e43249ef25fc4da49c363aec409953cd64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:292b8380d247e9ac7d575be970a46b0a90e4568fa92841ebd697d87c1240d9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23708396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922522fecc436cb20f7040b0227e8dc8c46b5f9ac9981d9425fb52d2ab0d397`

```dockerfile
```

-	Layers:
	-	`sha256:6f10a08a03a11cd3796fdc3b6159f068cf58a7b55c4910257a8d3300f71e55e9`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 23.7 MB (23691911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb23ec2ff4e9d03fd8af8d8d1f01c4a5c73fdbd14991061c2dd3fac91a32092c`  
		Last Modified: Fri, 14 Nov 2025 02:18:09 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:41fcc905f0f9a4457176b13c45cdf96aa4ca78e87c5f763bbcb4ba258c2a1119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1b7bc03289086014c668f8ccbe79e695b7f9fa664f2051244fb533876a369136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141523928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e99193c4c42d72a55a8eeb26d95b92f9a7f9af8346609b53d94bc893fefc11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:57ee80c600998f8068442d113d8ee0807739ea0cee8a65b156ac18446ec45740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17673284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc69088c126bb40646628a29e6042c71b1ef516c177b297846f1b3e501c680a4`

```dockerfile
```

-	Layers:
	-	`sha256:535aba84158df29180f4d18bcf63138b4978a8857127d895ae421b3178d05351`  
		Last Modified: Fri, 14 Nov 2025 02:17:56 GMT  
		Size: 17.7 MB (17658670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f247ca3c0dd8eb3914bb57ace0c3123fb7aed0a60249243405bf499b7297d951`  
		Last Modified: Fri, 14 Nov 2025 02:17:57 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d310b586219f0b7d8f2aa5ce679665a8af4419f46764657ef98ed57ff59afa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137075606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a19568c32acb20a4beceb411c7f804c416477cdf0650b552bcd3b6ccaa48b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:b28ade8a1be229037c3460e86d228d12aec37861ea89367f43b2555aa64eb72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17659754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc44cf26dd1a8be6ed576aeb6e90218d77a16a5fdf113460581a48a4b72ae61`

```dockerfile
```

-	Layers:
	-	`sha256:5efcbfc6973cc010f2b29699d4069d9dd1e31ed9002c537e0f7f4890ff52ff6d`  
		Last Modified: Fri, 14 Nov 2025 02:18:13 GMT  
		Size: 17.6 MB (17645015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8c54a7e88ccb06665fc5ccd966a53155e343cf9ff7e93db8a779a4656afd18`  
		Last Modified: Fri, 14 Nov 2025 02:18:14 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:41fcc905f0f9a4457176b13c45cdf96aa4ca78e87c5f763bbcb4ba258c2a1119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1b7bc03289086014c668f8ccbe79e695b7f9fa664f2051244fb533876a369136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141523928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e99193c4c42d72a55a8eeb26d95b92f9a7f9af8346609b53d94bc893fefc11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:57ee80c600998f8068442d113d8ee0807739ea0cee8a65b156ac18446ec45740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17673284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc69088c126bb40646628a29e6042c71b1ef516c177b297846f1b3e501c680a4`

```dockerfile
```

-	Layers:
	-	`sha256:535aba84158df29180f4d18bcf63138b4978a8857127d895ae421b3178d05351`  
		Last Modified: Fri, 14 Nov 2025 02:17:56 GMT  
		Size: 17.7 MB (17658670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f247ca3c0dd8eb3914bb57ace0c3123fb7aed0a60249243405bf499b7297d951`  
		Last Modified: Fri, 14 Nov 2025 02:17:57 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d310b586219f0b7d8f2aa5ce679665a8af4419f46764657ef98ed57ff59afa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137075606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a19568c32acb20a4beceb411c7f804c416477cdf0650b552bcd3b6ccaa48b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:b28ade8a1be229037c3460e86d228d12aec37861ea89367f43b2555aa64eb72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17659754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc44cf26dd1a8be6ed576aeb6e90218d77a16a5fdf113460581a48a4b72ae61`

```dockerfile
```

-	Layers:
	-	`sha256:5efcbfc6973cc010f2b29699d4069d9dd1e31ed9002c537e0f7f4890ff52ff6d`  
		Last Modified: Fri, 14 Nov 2025 02:18:13 GMT  
		Size: 17.6 MB (17645015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8c54a7e88ccb06665fc5ccd966a53155e343cf9ff7e93db8a779a4656afd18`  
		Last Modified: Fri, 14 Nov 2025 02:18:14 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:23ac13cf396221df5cd83dd0b636d920b23ed9b0651c25ba061c0881a90de458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:fdfa5ace8d17e58758391a86579b8e59eb8be21ce6461ae34311dc9854178342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080404531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f17afa977e9553bf8f9d364af72bbbc94a03684c231ebe65e75e3420c16111b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bace735bfd1b5a18bc9885894ac02044ab2640d66910d38779034a0f110c984a`  
		Last Modified: Fri, 14 Nov 2025 05:46:26 GMT  
		Size: 784.5 MB (784466755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:5da1f098830431730c35068caf61beb59e75268e96b28158e3af6be140b246b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8127ae88fe25268781a0baac627c8d614e8de9bf7c94b195d98770541698c6e`

```dockerfile
```

-	Layers:
	-	`sha256:a0aae68ce3687e68b79a811d89042cea004876b89bc43c7b058ee6e1be35956d`  
		Last Modified: Fri, 14 Nov 2025 05:17:53 GMT  
		Size: 60.7 MB (60706022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78dc0fdcdbe6caa1e02fcc1bb56ec272f8bde016e1d8f49fba170da78496c021`  
		Last Modified: Fri, 14 Nov 2025 05:17:55 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:938f6facaf3810263df124947e631d03e075f5c535f56263274bceae993b75cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.9 MB (978876409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d90f810db0dd1f5f69d47386e8b01c828cde37a2545a362e14a97276f499e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f7f5e89623d6ff02f526197860623344d614b00161b33893d9822c2cced15`  
		Last Modified: Fri, 14 Nov 2025 10:37:16 GMT  
		Size: 694.5 MB (694492997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:4e1ffd49122ba0d4cd551a720ad25a563c6d760cf536511898c390c807b819dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f44731e791978aefb0dd67afb2c84b5951cc6ef71452f4ff0f500a15123f0c`

```dockerfile
```

-	Layers:
	-	`sha256:4d7f0359dd9afa8d1d7b4f1a150ae315c5e631d568fe619014ce90bbe8a7c5a0`  
		Last Modified: Fri, 14 Nov 2025 05:19:19 GMT  
		Size: 60.6 MB (60636547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234858944fcb5e1cc376a120a72ad87bb19b675630a0be21aca85e44b0c454d4`  
		Last Modified: Fri, 14 Nov 2025 05:19:20 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:23ac13cf396221df5cd83dd0b636d920b23ed9b0651c25ba061c0881a90de458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:fdfa5ace8d17e58758391a86579b8e59eb8be21ce6461ae34311dc9854178342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080404531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f17afa977e9553bf8f9d364af72bbbc94a03684c231ebe65e75e3420c16111b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bace735bfd1b5a18bc9885894ac02044ab2640d66910d38779034a0f110c984a`  
		Last Modified: Fri, 14 Nov 2025 05:46:26 GMT  
		Size: 784.5 MB (784466755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5da1f098830431730c35068caf61beb59e75268e96b28158e3af6be140b246b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8127ae88fe25268781a0baac627c8d614e8de9bf7c94b195d98770541698c6e`

```dockerfile
```

-	Layers:
	-	`sha256:a0aae68ce3687e68b79a811d89042cea004876b89bc43c7b058ee6e1be35956d`  
		Last Modified: Fri, 14 Nov 2025 05:17:53 GMT  
		Size: 60.7 MB (60706022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78dc0fdcdbe6caa1e02fcc1bb56ec272f8bde016e1d8f49fba170da78496c021`  
		Last Modified: Fri, 14 Nov 2025 05:17:55 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:938f6facaf3810263df124947e631d03e075f5c535f56263274bceae993b75cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.9 MB (978876409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d90f810db0dd1f5f69d47386e8b01c828cde37a2545a362e14a97276f499e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f7f5e89623d6ff02f526197860623344d614b00161b33893d9822c2cced15`  
		Last Modified: Fri, 14 Nov 2025 10:37:16 GMT  
		Size: 694.5 MB (694492997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4e1ffd49122ba0d4cd551a720ad25a563c6d760cf536511898c390c807b819dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f44731e791978aefb0dd67afb2c84b5951cc6ef71452f4ff0f500a15123f0c`

```dockerfile
```

-	Layers:
	-	`sha256:4d7f0359dd9afa8d1d7b4f1a150ae315c5e631d568fe619014ce90bbe8a7c5a0`  
		Last Modified: Fri, 14 Nov 2025 05:19:19 GMT  
		Size: 60.6 MB (60636547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234858944fcb5e1cc376a120a72ad87bb19b675630a0be21aca85e44b0c454d4`  
		Last Modified: Fri, 14 Nov 2025 05:19:20 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:467a18374bb776485a1720fc68400b5ed1bac94defd59064e881f3f05f1631c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c420ad6abf1e51f3fdf82a69e107601c4a9e0ef4433fb446cb0bcd829c2cc3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157370334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2944457b1a8ed0d61ede200277c61c7d8cee537cf0efebb74d5af34807313e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:aa6f6782fb8809d1bdc11cc0c39268ca1f92a4361dde84b2144d0f6d757bbe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2aec48da4050c47322daa0c5d5b229e2dd930655ef7535791496ec90d58b25`

```dockerfile
```

-	Layers:
	-	`sha256:82536b918e41be2698e73a79e1d27e387ec53ce1fc2c9d80f9147f2deede39c8`  
		Last Modified: Fri, 14 Nov 2025 02:18:29 GMT  
		Size: 18.3 MB (18300584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedbc50bfebc9bcdaa2e2ffde4d36995eea034731102d1d2c38550bf4ca41bd2`  
		Last Modified: Fri, 14 Nov 2025 02:18:31 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f89dfa391a2e2e87e7d9ece24fafd916df612422c1917fcd6db0cf9285e5d139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151307684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281158ddbed9d2ece10045e53849ad1a4014acfeaedd71e8596c82e203918f10`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:598a7a2553b79860a5e1507079e269b151f344672a5245e849678eb8148d808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cbd7d7c2a1bec5bfedf88f6bc329b070c59adb966e6f536249e99e6ed7afe6`

```dockerfile
```

-	Layers:
	-	`sha256:76bd73b0f67cbb130195955194720d3f9ae34819328c3d09aa28ff0e95eb181a`  
		Last Modified: Fri, 14 Nov 2025 02:18:45 GMT  
		Size: 18.3 MB (18274590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042300afc3122faebbb64fad817226bc3428cc12a33bec01b770a4136c6bedeb`  
		Last Modified: Fri, 14 Nov 2025 02:18:46 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:467a18374bb776485a1720fc68400b5ed1bac94defd59064e881f3f05f1631c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c420ad6abf1e51f3fdf82a69e107601c4a9e0ef4433fb446cb0bcd829c2cc3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157370334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2944457b1a8ed0d61ede200277c61c7d8cee537cf0efebb74d5af34807313e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:aa6f6782fb8809d1bdc11cc0c39268ca1f92a4361dde84b2144d0f6d757bbe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2aec48da4050c47322daa0c5d5b229e2dd930655ef7535791496ec90d58b25`

```dockerfile
```

-	Layers:
	-	`sha256:82536b918e41be2698e73a79e1d27e387ec53ce1fc2c9d80f9147f2deede39c8`  
		Last Modified: Fri, 14 Nov 2025 02:18:29 GMT  
		Size: 18.3 MB (18300584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedbc50bfebc9bcdaa2e2ffde4d36995eea034731102d1d2c38550bf4ca41bd2`  
		Last Modified: Fri, 14 Nov 2025 02:18:31 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f89dfa391a2e2e87e7d9ece24fafd916df612422c1917fcd6db0cf9285e5d139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151307684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281158ddbed9d2ece10045e53849ad1a4014acfeaedd71e8596c82e203918f10`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:598a7a2553b79860a5e1507079e269b151f344672a5245e849678eb8148d808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cbd7d7c2a1bec5bfedf88f6bc329b070c59adb966e6f536249e99e6ed7afe6`

```dockerfile
```

-	Layers:
	-	`sha256:76bd73b0f67cbb130195955194720d3f9ae34819328c3d09aa28ff0e95eb181a`  
		Last Modified: Fri, 14 Nov 2025 02:18:45 GMT  
		Size: 18.3 MB (18274590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042300afc3122faebbb64fad817226bc3428cc12a33bec01b770a4136c6bedeb`  
		Last Modified: Fri, 14 Nov 2025 02:18:46 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:300c9505e7261fc80d1aa75c3b1b4beabad4223329ff9d9cd41f608f794df243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:0cc6b0e7d3502ad36eeefc5143505caa15c34cc9f5ab554738732a25b0d917f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311030510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b55dbd0930b08c6f1b091089737b918a73cd9b17a8d0e6d2780cce35b15bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:0c96703cc6405f14d42e6348a531553c713f4c179dda4974ad64c2f60aeafd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64817ffa8ae718817fbbf00fb0576b8bc53dff162855c53d975b2f3bbb98c32`

```dockerfile
```

-	Layers:
	-	`sha256:5709b9ba52bdf82559bb29618ebccf96f4b01358b316409e5f9d82a413f91448`  
		Last Modified: Fri, 14 Nov 2025 02:18:35 GMT  
		Size: 24.7 MB (24650335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7692c8f6f42bdae33ec2302b3a1c6c86524cf78aede683f6edfb91f5b09a8d75`  
		Last Modified: Fri, 14 Nov 2025 02:18:36 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfc7ec8e8eb439842ca4bcd2f56faa2d0d9b62accad6d220a0985288dc119db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299376599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899ee8dff90370a8507bd0b1f9315f5203e2085e259642ff4e929efa5246cd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:d1f76759f0ac3ca705dcc4a37e8c233beb36ac6917e0bc2ef1eba4bcf07871e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a76dd5e9d7e6883d644c5b0b55de743605a2cf961ccac1deb7217ade910f6`

```dockerfile
```

-	Layers:
	-	`sha256:c9e538338867200639c593c1d6b3397b23eae1eddaea021ddeab641705c00a5d`  
		Last Modified: Fri, 14 Nov 2025 02:18:59 GMT  
		Size: 24.7 MB (24672596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91de0fa134b2151a75b51f9e4355bbf5e8746ee15d6a76f7bb13ef422a45bfb`  
		Last Modified: Fri, 14 Nov 2025 02:19:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:597eb7c1b6ef46d03c1306786771714cef4064d5654887ca996713712185a190
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:39acb6f9dbe66091f760eb26611744af06f98cc62d21a8ebb6e826ceea4ab104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095999495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3065d8b3834d1c8b2fa54e8585dca47f3a383187ecf1ab1ad05190a0ea929`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6b475c9d5d0fec8f295a27b9c88c7e104854439857ec2508c68a04327c933`  
		Last Modified: Fri, 14 Nov 2025 05:51:37 GMT  
		Size: 785.0 MB (784968985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:49b431be399ca5fe716018c10a722888c1fa293c5be0710962d4a84c3257101b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e84ea6271ee0ddf4c85b11145a84b6e7efe869fc8a1a05673e392f0ef2c1a`

```dockerfile
```

-	Layers:
	-	`sha256:4846b83d86f5b32056c650890347f732ff8a4c09aaad50f312de07d40693ab51`  
		Last Modified: Fri, 14 Nov 2025 05:18:06 GMT  
		Size: 60.8 MB (60822416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e11511c30e26ba831e3130603c6135fa399dce361debb54e7debc7755ac46e`  
		Last Modified: Fri, 14 Nov 2025 05:18:08 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d69e6b68fbf0b451f2d2916f8320507c33e47620dea9c9609ff663bb0e5bd47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.3 MB (994340523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67faf80aeacd3fac0059ebc1e8ab26ce58f1016a22fea364f281a5d6103c1f51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ec05d315c3cb7241734afa22b2b434a0e74d932c29d5d3e00d0d27e8b1a342`  
		Last Modified: Fri, 14 Nov 2025 06:02:24 GMT  
		Size: 695.0 MB (694963924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:03337ba5432546dcb0a55a48d697155319d747795cc06ec0447dcc510d22d2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760579d59a40d6d4b825b88fe7a6a01c47c48a4ac352b70eb03ac1622161c190`

```dockerfile
```

-	Layers:
	-	`sha256:d5dc70d9db7a43715963e98a03df7919d4e1749a716a4262a67bba890d0ce0e7`  
		Last Modified: Fri, 14 Nov 2025 05:19:34 GMT  
		Size: 60.8 MB (60752941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813bbfb4e7dd5d9cfaffd99d1a7feba515a6390671be13bda5c0949e7effd486`  
		Last Modified: Fri, 14 Nov 2025 05:19:35 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:597eb7c1b6ef46d03c1306786771714cef4064d5654887ca996713712185a190
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:39acb6f9dbe66091f760eb26611744af06f98cc62d21a8ebb6e826ceea4ab104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095999495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3065d8b3834d1c8b2fa54e8585dca47f3a383187ecf1ab1ad05190a0ea929`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6b475c9d5d0fec8f295a27b9c88c7e104854439857ec2508c68a04327c933`  
		Last Modified: Fri, 14 Nov 2025 05:51:37 GMT  
		Size: 785.0 MB (784968985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:49b431be399ca5fe716018c10a722888c1fa293c5be0710962d4a84c3257101b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e84ea6271ee0ddf4c85b11145a84b6e7efe869fc8a1a05673e392f0ef2c1a`

```dockerfile
```

-	Layers:
	-	`sha256:4846b83d86f5b32056c650890347f732ff8a4c09aaad50f312de07d40693ab51`  
		Last Modified: Fri, 14 Nov 2025 05:18:06 GMT  
		Size: 60.8 MB (60822416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e11511c30e26ba831e3130603c6135fa399dce361debb54e7debc7755ac46e`  
		Last Modified: Fri, 14 Nov 2025 05:18:08 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d69e6b68fbf0b451f2d2916f8320507c33e47620dea9c9609ff663bb0e5bd47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.3 MB (994340523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67faf80aeacd3fac0059ebc1e8ab26ce58f1016a22fea364f281a5d6103c1f51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ec05d315c3cb7241734afa22b2b434a0e74d932c29d5d3e00d0d27e8b1a342`  
		Last Modified: Fri, 14 Nov 2025 06:02:24 GMT  
		Size: 695.0 MB (694963924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:03337ba5432546dcb0a55a48d697155319d747795cc06ec0447dcc510d22d2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760579d59a40d6d4b825b88fe7a6a01c47c48a4ac352b70eb03ac1622161c190`

```dockerfile
```

-	Layers:
	-	`sha256:d5dc70d9db7a43715963e98a03df7919d4e1749a716a4262a67bba890d0ce0e7`  
		Last Modified: Fri, 14 Nov 2025 05:19:34 GMT  
		Size: 60.8 MB (60752941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813bbfb4e7dd5d9cfaffd99d1a7feba515a6390671be13bda5c0949e7effd486`  
		Last Modified: Fri, 14 Nov 2025 05:19:35 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:300c9505e7261fc80d1aa75c3b1b4beabad4223329ff9d9cd41f608f794df243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0cc6b0e7d3502ad36eeefc5143505caa15c34cc9f5ab554738732a25b0d917f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311030510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b55dbd0930b08c6f1b091089737b918a73cd9b17a8d0e6d2780cce35b15bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0c96703cc6405f14d42e6348a531553c713f4c179dda4974ad64c2f60aeafd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64817ffa8ae718817fbbf00fb0576b8bc53dff162855c53d975b2f3bbb98c32`

```dockerfile
```

-	Layers:
	-	`sha256:5709b9ba52bdf82559bb29618ebccf96f4b01358b316409e5f9d82a413f91448`  
		Last Modified: Fri, 14 Nov 2025 02:18:35 GMT  
		Size: 24.7 MB (24650335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7692c8f6f42bdae33ec2302b3a1c6c86524cf78aede683f6edfb91f5b09a8d75`  
		Last Modified: Fri, 14 Nov 2025 02:18:36 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfc7ec8e8eb439842ca4bcd2f56faa2d0d9b62accad6d220a0985288dc119db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299376599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899ee8dff90370a8507bd0b1f9315f5203e2085e259642ff4e929efa5246cd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d1f76759f0ac3ca705dcc4a37e8c233beb36ac6917e0bc2ef1eba4bcf07871e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a76dd5e9d7e6883d644c5b0b55de743605a2cf961ccac1deb7217ade910f6`

```dockerfile
```

-	Layers:
	-	`sha256:c9e538338867200639c593c1d6b3397b23eae1eddaea021ddeab641705c00a5d`  
		Last Modified: Fri, 14 Nov 2025 02:18:59 GMT  
		Size: 24.7 MB (24672596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91de0fa134b2151a75b51f9e4355bbf5e8746ee15d6a76f7bb13ef422a45bfb`  
		Last Modified: Fri, 14 Nov 2025 02:19:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:300c9505e7261fc80d1aa75c3b1b4beabad4223329ff9d9cd41f608f794df243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:0cc6b0e7d3502ad36eeefc5143505caa15c34cc9f5ab554738732a25b0d917f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311030510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b55dbd0930b08c6f1b091089737b918a73cd9b17a8d0e6d2780cce35b15bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0c96703cc6405f14d42e6348a531553c713f4c179dda4974ad64c2f60aeafd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64817ffa8ae718817fbbf00fb0576b8bc53dff162855c53d975b2f3bbb98c32`

```dockerfile
```

-	Layers:
	-	`sha256:5709b9ba52bdf82559bb29618ebccf96f4b01358b316409e5f9d82a413f91448`  
		Last Modified: Fri, 14 Nov 2025 02:18:35 GMT  
		Size: 24.7 MB (24650335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7692c8f6f42bdae33ec2302b3a1c6c86524cf78aede683f6edfb91f5b09a8d75`  
		Last Modified: Fri, 14 Nov 2025 02:18:36 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfc7ec8e8eb439842ca4bcd2f56faa2d0d9b62accad6d220a0985288dc119db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299376599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899ee8dff90370a8507bd0b1f9315f5203e2085e259642ff4e929efa5246cd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d1f76759f0ac3ca705dcc4a37e8c233beb36ac6917e0bc2ef1eba4bcf07871e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a76dd5e9d7e6883d644c5b0b55de743605a2cf961ccac1deb7217ade910f6`

```dockerfile
```

-	Layers:
	-	`sha256:c9e538338867200639c593c1d6b3397b23eae1eddaea021ddeab641705c00a5d`  
		Last Modified: Fri, 14 Nov 2025 02:18:59 GMT  
		Size: 24.7 MB (24672596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91de0fa134b2151a75b51f9e4355bbf5e8746ee15d6a76f7bb13ef422a45bfb`  
		Last Modified: Fri, 14 Nov 2025 02:19:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:7221a3ace60bd89dcdbab43b4b1c0dc29ae4e00fb3ab89fd53cdfb5725cbdf5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:71dffd91d6e05f2e6fb45a8f7c50adcc2779d07a91595905ec03e5a810199301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172415875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11db19880322bbd67862dfc2668cc144ef548aad87cd147f492b537f99c1a71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:d683b1784008e72cb46ee49f7aa1d28df7c5ef4d1b6dd66ff304a4b62851ee57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18414499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cb14a7e3cce46457f63428bed76fd754b0b6abfced533286faed0b625530fa`

```dockerfile
```

-	Layers:
	-	`sha256:e4985fd057570c468fc96bb62df258c03eab74a70dc3c1c4c9bb61c9031c5c57`  
		Last Modified: Fri, 14 Nov 2025 02:18:47 GMT  
		Size: 18.4 MB (18399890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9eb7602ba2f229898a075b0bb9ccb526ee341b72841cac812ee928dd4c276b`  
		Last Modified: Fri, 14 Nov 2025 02:18:48 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fc8363ba6068263da3fbe69ff00c316ac5ab301e59a29b22af32a39c6f6fcc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166270581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c070658d53fb2c816128f320b7611bd518d5c72fa0e1e202f7447826935b244`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:e77fe1c1ab6c85d180018fe72ed0ae259123b544157dd5fada0b6bf56dab92aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18388630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562cb007d439e1943b0dc24fb0a7f7cbd3b63be2f92b1420520b1965411c3055`

```dockerfile
```

-	Layers:
	-	`sha256:b1d52c2f0d04c47a47a556afa1e39562421798149d31731cf700f01b96548d1b`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 18.4 MB (18373896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1c6e57343393f4961be238044bd8bdb6d721666a95455baced9aeac752aad7`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:7221a3ace60bd89dcdbab43b4b1c0dc29ae4e00fb3ab89fd53cdfb5725cbdf5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:71dffd91d6e05f2e6fb45a8f7c50adcc2779d07a91595905ec03e5a810199301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172415875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11db19880322bbd67862dfc2668cc144ef548aad87cd147f492b537f99c1a71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d683b1784008e72cb46ee49f7aa1d28df7c5ef4d1b6dd66ff304a4b62851ee57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18414499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cb14a7e3cce46457f63428bed76fd754b0b6abfced533286faed0b625530fa`

```dockerfile
```

-	Layers:
	-	`sha256:e4985fd057570c468fc96bb62df258c03eab74a70dc3c1c4c9bb61c9031c5c57`  
		Last Modified: Fri, 14 Nov 2025 02:18:47 GMT  
		Size: 18.4 MB (18399890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9eb7602ba2f229898a075b0bb9ccb526ee341b72841cac812ee928dd4c276b`  
		Last Modified: Fri, 14 Nov 2025 02:18:48 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fc8363ba6068263da3fbe69ff00c316ac5ab301e59a29b22af32a39c6f6fcc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166270581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c070658d53fb2c816128f320b7611bd518d5c72fa0e1e202f7447826935b244`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e77fe1c1ab6c85d180018fe72ed0ae259123b544157dd5fada0b6bf56dab92aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18388630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562cb007d439e1943b0dc24fb0a7f7cbd3b63be2f92b1420520b1965411c3055`

```dockerfile
```

-	Layers:
	-	`sha256:b1d52c2f0d04c47a47a556afa1e39562421798149d31731cf700f01b96548d1b`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 18.4 MB (18373896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1c6e57343393f4961be238044bd8bdb6d721666a95455baced9aeac752aad7`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:029b235468abbd489780a439ae35b739bd05a42edb5c5f10f3e1b3db30300f36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:f414f0f55ca18ecd31844deff5e7697d982790844e447b13a6450f6271592997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324675620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41af6baddc4abfe59e2d6f0cf880a9a9b36c18d8411d5ee7164aafada8498f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:66ddeffd7daf51f32eabea4b4f291a53e86fc95d72aa6df4af2dd0ca9a76ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25740803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df47cab50819f0c219786a9e845ce6ac771bb36997070a09d31f320b6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:71c54244bdb403b3d6b44098fafb232e6f53cbbb40ade9e8486caab58fa02dc0`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 25.7 MB (25724438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c9352a53a21487108f4767012a0672567fca97fed315ee748096c737db26b`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28fd4ade8c7eeceef74187f01cf26800f5d7c67ff22f62fa27a16b65746aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312650455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf90b6fa04814069b7cc74317cdd9f3421e7b712843f32141043c5a76571cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:fb6bccc15b557ab67edb1d332e3a80ade8893c2865d1fc4f5c4bceb31e487a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25763398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41117bc44e3f37051e031a19cc2981fd6dc98b44d7b0a5d736009df486bc0eb`

```dockerfile
```

-	Layers:
	-	`sha256:e94a7abd29f5ed0717d069409d1949ec6ce56cee5dea8dbc3aca8199a0894a25`  
		Last Modified: Fri, 14 Nov 2025 02:19:27 GMT  
		Size: 25.7 MB (25746896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6bfa8cb739cd81e1891288b2e14a5ec0f76cc16c406310bc7fc5d4f551b125`  
		Last Modified: Fri, 14 Nov 2025 02:19:28 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:e15e22a7b12d83bd8e74a87010080adb9c697187a4e7919b3f1107b0dec458f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:be9194c01daebb513760ea0807f691b37f62841a4a5be177ec3222524e330fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1109207168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b2635343eeff54fff474edeafc2f1dadfc528f4d028fd9c95b354832a3130`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9384e3c026a30291bf2ecbebae43f7737e26f758c5e65826a7d7988f7ac77`  
		Last Modified: Fri, 14 Nov 2025 07:35:37 GMT  
		Size: 784.5 MB (784531548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:8ca951d20e89c222764cbcb0b4331902ba1c3b085a4bf2f39dd6365614ed4b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61913258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2947e13ed1bac2da29d09b83220014ae1b8a2ededb2169110dc3fd7a4c1db3`

```dockerfile
```

-	Layers:
	-	`sha256:52578280739f10315a8e65bdc4774e09575922556d6a284cdd6e14c9d8b27acf`  
		Last Modified: Fri, 14 Nov 2025 05:18:20 GMT  
		Size: 61.9 MB (61903897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf96a68f2d59ab1e7f9f8918eddc4c5eac8939a3bf23497a75c3746d4467f6f`  
		Last Modified: Fri, 14 Nov 2025 05:18:22 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:74c1149c7a5c1bef22da018fae466515e000a344da879394d76676e2c69b76ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007216187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bda908390a724e838225ade5c6d650df196f05eb7cf27a5828bb628444179b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ce4a548a9e278afac869dc062059bbbf762381ef3136c4835c8f663eddb426`  
		Last Modified: Fri, 14 Nov 2025 15:50:51 GMT  
		Size: 694.6 MB (694565732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:ed822594c7d69eb4c75dabd13d741dd7cc5b5eb3949da7e742836660fcbcccf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61844060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925f4f20ea9d6203be5ef243fa96c9321d6ce00d17aa52eecdd9449ed120bd00`

```dockerfile
```

-	Layers:
	-	`sha256:a42fa6f66f50eaaf261bb413c076f2545dfc6ff742ef782c9f519d25ba3e9d10`  
		Last Modified: Fri, 14 Nov 2025 05:20:09 GMT  
		Size: 61.8 MB (61834619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ed22bcee0de118946955cada52b3078043306650cacd0d92f09dd9b709e64f`  
		Last Modified: Fri, 14 Nov 2025 05:20:11 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:e15e22a7b12d83bd8e74a87010080adb9c697187a4e7919b3f1107b0dec458f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:be9194c01daebb513760ea0807f691b37f62841a4a5be177ec3222524e330fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1109207168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b2635343eeff54fff474edeafc2f1dadfc528f4d028fd9c95b354832a3130`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9384e3c026a30291bf2ecbebae43f7737e26f758c5e65826a7d7988f7ac77`  
		Last Modified: Fri, 14 Nov 2025 07:35:37 GMT  
		Size: 784.5 MB (784531548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8ca951d20e89c222764cbcb0b4331902ba1c3b085a4bf2f39dd6365614ed4b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61913258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2947e13ed1bac2da29d09b83220014ae1b8a2ededb2169110dc3fd7a4c1db3`

```dockerfile
```

-	Layers:
	-	`sha256:52578280739f10315a8e65bdc4774e09575922556d6a284cdd6e14c9d8b27acf`  
		Last Modified: Fri, 14 Nov 2025 05:18:20 GMT  
		Size: 61.9 MB (61903897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf96a68f2d59ab1e7f9f8918eddc4c5eac8939a3bf23497a75c3746d4467f6f`  
		Last Modified: Fri, 14 Nov 2025 05:18:22 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:74c1149c7a5c1bef22da018fae466515e000a344da879394d76676e2c69b76ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007216187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bda908390a724e838225ade5c6d650df196f05eb7cf27a5828bb628444179b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ce4a548a9e278afac869dc062059bbbf762381ef3136c4835c8f663eddb426`  
		Last Modified: Fri, 14 Nov 2025 15:50:51 GMT  
		Size: 694.6 MB (694565732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ed822594c7d69eb4c75dabd13d741dd7cc5b5eb3949da7e742836660fcbcccf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61844060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925f4f20ea9d6203be5ef243fa96c9321d6ce00d17aa52eecdd9449ed120bd00`

```dockerfile
```

-	Layers:
	-	`sha256:a42fa6f66f50eaaf261bb413c076f2545dfc6ff742ef782c9f519d25ba3e9d10`  
		Last Modified: Fri, 14 Nov 2025 05:20:09 GMT  
		Size: 61.8 MB (61834619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ed22bcee0de118946955cada52b3078043306650cacd0d92f09dd9b709e64f`  
		Last Modified: Fri, 14 Nov 2025 05:20:11 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:029b235468abbd489780a439ae35b739bd05a42edb5c5f10f3e1b3db30300f36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:f414f0f55ca18ecd31844deff5e7697d982790844e447b13a6450f6271592997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324675620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41af6baddc4abfe59e2d6f0cf880a9a9b36c18d8411d5ee7164aafada8498f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:66ddeffd7daf51f32eabea4b4f291a53e86fc95d72aa6df4af2dd0ca9a76ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25740803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df47cab50819f0c219786a9e845ce6ac771bb36997070a09d31f320b6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:71c54244bdb403b3d6b44098fafb232e6f53cbbb40ade9e8486caab58fa02dc0`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 25.7 MB (25724438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c9352a53a21487108f4767012a0672567fca97fed315ee748096c737db26b`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28fd4ade8c7eeceef74187f01cf26800f5d7c67ff22f62fa27a16b65746aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312650455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf90b6fa04814069b7cc74317cdd9f3421e7b712843f32141043c5a76571cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fb6bccc15b557ab67edb1d332e3a80ade8893c2865d1fc4f5c4bceb31e487a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25763398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41117bc44e3f37051e031a19cc2981fd6dc98b44d7b0a5d736009df486bc0eb`

```dockerfile
```

-	Layers:
	-	`sha256:e94a7abd29f5ed0717d069409d1949ec6ce56cee5dea8dbc3aca8199a0894a25`  
		Last Modified: Fri, 14 Nov 2025 02:19:27 GMT  
		Size: 25.7 MB (25746896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6bfa8cb739cd81e1891288b2e14a5ec0f76cc16c406310bc7fc5d4f551b125`  
		Last Modified: Fri, 14 Nov 2025 02:19:28 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:029b235468abbd489780a439ae35b739bd05a42edb5c5f10f3e1b3db30300f36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:f414f0f55ca18ecd31844deff5e7697d982790844e447b13a6450f6271592997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324675620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41af6baddc4abfe59e2d6f0cf880a9a9b36c18d8411d5ee7164aafada8498f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:66ddeffd7daf51f32eabea4b4f291a53e86fc95d72aa6df4af2dd0ca9a76ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25740803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df47cab50819f0c219786a9e845ce6ac771bb36997070a09d31f320b6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:71c54244bdb403b3d6b44098fafb232e6f53cbbb40ade9e8486caab58fa02dc0`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 25.7 MB (25724438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c9352a53a21487108f4767012a0672567fca97fed315ee748096c737db26b`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28fd4ade8c7eeceef74187f01cf26800f5d7c67ff22f62fa27a16b65746aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312650455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf90b6fa04814069b7cc74317cdd9f3421e7b712843f32141043c5a76571cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fb6bccc15b557ab67edb1d332e3a80ade8893c2865d1fc4f5c4bceb31e487a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25763398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41117bc44e3f37051e031a19cc2981fd6dc98b44d7b0a5d736009df486bc0eb`

```dockerfile
```

-	Layers:
	-	`sha256:e94a7abd29f5ed0717d069409d1949ec6ce56cee5dea8dbc3aca8199a0894a25`  
		Last Modified: Fri, 14 Nov 2025 02:19:27 GMT  
		Size: 25.7 MB (25746896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6bfa8cb739cd81e1891288b2e14a5ec0f76cc16c406310bc7fc5d4f551b125`  
		Last Modified: Fri, 14 Nov 2025 02:19:28 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:93b84a38701fceb5d2b3bb1af7c5e63f8c7106f97334988ebf3244751202214a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:060cbce5038073f7d5a63629be758b379639ab8ace7e068c5b210e41185b7ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186323097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0ba5853c1c34d18315354e9621dd98fa71117cd372d3f383518a4158523450`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ebc496359d848b519a2da908b7e10b3f4e11e9c830bbc698ed802bb0113e5f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19490117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aadcd78feaae35a9e17bd1fe13b7fe468a146a513dfbaafb127910cd7db7ff3`

```dockerfile
```

-	Layers:
	-	`sha256:250c3cc3dad4910e142f62d5761d9543093cb4dc804858bd1066deca41ca6719`  
		Last Modified: Fri, 14 Nov 2025 02:19:13 GMT  
		Size: 19.5 MB (19475496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6393b8b9aac1f57c4a22cbbabae5a9bdfe54987e996408957e2be50cdab1aa`  
		Last Modified: Fri, 14 Nov 2025 02:19:14 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3460929d04dcdb8665ce9145d51cc2a63fbd6aa6db4fe992a62371260a7e3296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179799404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ea179f9f5087f290e587f9d4208ccbdd6380c75efe8473f697716b52c26d4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:dde8b3acc1adbc96d591369682c585f9deafa73dd52bcd5903ec7fa80bae38c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19464446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d86f9d7077bae3423cb51daf8d9fe4b8740853d101a14a625907c0813a7dc47`

```dockerfile
```

-	Layers:
	-	`sha256:d3acc2ae7593ba1acb6e43436377a32994a41c71db40800d21fc59107a451ddc`  
		Last Modified: Fri, 14 Nov 2025 02:19:30 GMT  
		Size: 19.4 MB (19449700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed016523c0ff6ea390cde8313cc9344362a8235fd5fc0f4520262916d62dd716`  
		Last Modified: Fri, 14 Nov 2025 02:19:31 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:93b84a38701fceb5d2b3bb1af7c5e63f8c7106f97334988ebf3244751202214a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:060cbce5038073f7d5a63629be758b379639ab8ace7e068c5b210e41185b7ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186323097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0ba5853c1c34d18315354e9621dd98fa71117cd372d3f383518a4158523450`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ebc496359d848b519a2da908b7e10b3f4e11e9c830bbc698ed802bb0113e5f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19490117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aadcd78feaae35a9e17bd1fe13b7fe468a146a513dfbaafb127910cd7db7ff3`

```dockerfile
```

-	Layers:
	-	`sha256:250c3cc3dad4910e142f62d5761d9543093cb4dc804858bd1066deca41ca6719`  
		Last Modified: Fri, 14 Nov 2025 02:19:13 GMT  
		Size: 19.5 MB (19475496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6393b8b9aac1f57c4a22cbbabae5a9bdfe54987e996408957e2be50cdab1aa`  
		Last Modified: Fri, 14 Nov 2025 02:19:14 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3460929d04dcdb8665ce9145d51cc2a63fbd6aa6db4fe992a62371260a7e3296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179799404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ea179f9f5087f290e587f9d4208ccbdd6380c75efe8473f697716b52c26d4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:dde8b3acc1adbc96d591369682c585f9deafa73dd52bcd5903ec7fa80bae38c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19464446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d86f9d7077bae3423cb51daf8d9fe4b8740853d101a14a625907c0813a7dc47`

```dockerfile
```

-	Layers:
	-	`sha256:d3acc2ae7593ba1acb6e43436377a32994a41c71db40800d21fc59107a451ddc`  
		Last Modified: Fri, 14 Nov 2025 02:19:30 GMT  
		Size: 19.4 MB (19449700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed016523c0ff6ea390cde8313cc9344362a8235fd5fc0f4520262916d62dd716`  
		Last Modified: Fri, 14 Nov 2025 02:19:31 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json
