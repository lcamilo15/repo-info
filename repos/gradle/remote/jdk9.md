## `gradle:jdk9`

```console
$ docker pull gradle@sha256:3652cdd89cda11811995d0b06cbb1d4d4fc6eb76538072d86cc724bd6547dae5
```

-	Platforms:
	-	linux; amd64

### `gradle:jdk9` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330860850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97649fbfd01195b816eca82ec416131382c352b2fc68bd734262710e0c3318a`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 21 Mar 2017 18:31:29 GMT
ADD file:c8a621347a67ba4a8bb70860663bb66e3d9e758ad2d8e53eabce6274b5a6c77b in / 
# Tue, 21 Mar 2017 18:31:30 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 19:12:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:51:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:51:45 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Tue, 21 Mar 2017 22:51:46 GMT
ENV LANG=C.UTF-8
# Tue, 21 Mar 2017 22:51:47 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 21 Mar 2017 22:51:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-9-openjdk-amd64
# Tue, 21 Mar 2017 22:51:48 GMT
ENV JAVA_VERSION=9~b161
# Tue, 21 Mar 2017 22:51:49 GMT
ENV JAVA_DEBIAN_VERSION=9~b161-1
# Tue, 21 Mar 2017 22:52:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Mar 2017 18:38:59 GMT
CMD ["gradle"]
# Thu, 23 Mar 2017 18:39:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 23 Mar 2017 18:39:01 GMT
ENV GRADLE_VERSION=3.4
# Thu, 23 Mar 2017 18:39:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=72d0cd4dcdd5e3be165eb7cd7bbd25cf8968baf400323d9ab1bba622c3f72205
# Thu, 23 Mar 2017 18:39:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72d0cd4dcdd5e3be165eb7cd7bbd25cf8968baf400323d9ab1bba622c3f72205
RUN set -o errexit -o nounset 	&& echo "Downloading Gradle" 	&& wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip" 		&& echo "Checking download hash" 	&& echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check - 		&& echo "Installing Gradle" 	&& unzip gradle.zip 	&& rm gradle.zip 	&& mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/" 	&& ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle 		&& echo "Adding gradle user and group" 	&& groupadd --system --gid 1000 gradle 	&& useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle 	&& mkdir /home/gradle/.gradle 	&& chown --recursive gradle:gradle /home/gradle
# Thu, 23 Mar 2017 18:39:23 GMT
USER [gradle]
# Thu, 23 Mar 2017 18:39:24 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 23 Mar 2017 18:39:25 GMT
WORKDIR /home/gradle
# Thu, 23 Mar 2017 18:39:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72d0cd4dcdd5e3be165eb7cd7bbd25cf8968baf400323d9ab1bba622c3f72205
RUN set -o errexit -o nounset 	&& echo "Testing Gradle installation" 	&& gradle --version
```

-	Layers:
	-	`sha256:0d62cc759168569be1547237908d9f01ae76df507f508033feaed6291c60a06e`  
		Last Modified: Tue, 21 Mar 2017 18:44:16 GMT  
		Size: 44.3 MB (44268563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a452a4ba8c66e6b557070473289879410f055e30ac86e4cb9dd2d6f50f0685`  
		Last Modified: Tue, 21 Mar 2017 20:03:07 GMT  
		Size: 21.2 MB (21150746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fbfa5a51b31a9bd473e3d51a02d9d26c6e3681624b5fe0526e3de7ba6b7eac`  
		Last Modified: Tue, 21 Mar 2017 20:03:47 GMT  
		Size: 40.0 MB (40049369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c6d4dcde8a91252c5b59911856b40fa393f5c43555bb0ec30d0266373be7a8`  
		Last Modified: Thu, 23 Mar 2017 18:55:44 GMT  
		Size: 651.8 KB (651843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056b597bb0447460e5a3f9229e907f4519974fd1cafa3d2306d1ead4c1d61ef3`  
		Last Modified: Thu, 23 Mar 2017 18:55:42 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb44b26812eae902f12ad6e045bf43b2714ac28b5d6ad67cc65fb3861675132`  
		Last Modified: Thu, 23 Mar 2017 18:55:41 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93808fe9b2f98daceb36fd746d8ade3035e65cbb172b8a0e512425866ec3435`  
		Last Modified: Thu, 23 Mar 2017 18:56:07 GMT  
		Size: 154.5 MB (154476439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826db136282e651d8181a0c60fa3bf43da11f4282e3bf29fd0b39f7ce30bf705`  
		Last Modified: Thu, 23 Mar 2017 18:55:51 GMT  
		Size: 70.3 MB (70263297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c12205feded24840495327805115c6b94baa27e2adda44ef571540aa47923`  
		Last Modified: Thu, 23 Mar 2017 18:55:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
