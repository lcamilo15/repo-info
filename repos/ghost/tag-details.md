<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:0.11.7`](#ghost0117)
-	[`ghost:0.11`](#ghost011)
-	[`ghost:0`](#ghost0)
-	[`ghost:latest`](#ghostlatest)

## `ghost:0.11.7`

```console
$ docker pull ghost@sha256:0cf2fdcc10db488992cb764b40009d0da12f2f88957928758c2ca2e7ec94ee26
```

-	Platforms:
	-	linux; amd64

### `ghost:0.11.7` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111346590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e23922b175cd5ede2ff9539f16372880a857fae79f98480e2313d1f487e08c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:07:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 22 Mar 2017 23:53:28 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Wed, 22 Mar 2017 23:53:45 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 23 Mar 2017 00:28:34 GMT
ENV NODE_VERSION=4.8.1
# Thu, 23 Mar 2017 00:28:46 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 23 Mar 2017 00:28:46 GMT
ENV YARN_VERSION=0.21.3
# Thu, 23 Mar 2017 00:28:51 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done   && curl -fSL -o yarn.js "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js"   && curl -fSL -o yarn.js.asc "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js.asc"   && gpg --batch --verify yarn.js.asc yarn.js   && rm yarn.js.asc   && mv yarn.js /usr/local/bin/yarn   && chmod +x /usr/local/bin/yarn
# Thu, 23 Mar 2017 00:28:51 GMT
CMD ["node"]
# Thu, 23 Mar 2017 02:12:35 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Thu, 23 Mar 2017 02:12:36 GMT
ENV GOSU_VERSION=1.7
# Thu, 23 Mar 2017 02:12:40 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Thu, 23 Mar 2017 02:12:40 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Thu, 23 Mar 2017 02:12:40 GMT
WORKDIR /usr/src/ghost
# Thu, 23 Mar 2017 02:12:41 GMT
ENV GHOST_VERSION=0.11.7
# Thu, 23 Mar 2017 02:13:57 GMT
RUN buildDeps=' 		gcc 		make 		python 		unzip 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip" 	&& unzip ghost.zip 	&& npm install --production 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false $buildDeps 	&& rm ghost.zip 	&& npm cache clean 	&& rm -rf /tmp/npm*
# Thu, 23 Mar 2017 02:13:58 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Thu, 23 Mar 2017 02:13:59 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Thu, 23 Mar 2017 02:13:59 GMT
VOLUME [/var/lib/ghost]
# Thu, 23 Mar 2017 02:14:00 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /entrypoint.sh 
# Thu, 23 Mar 2017 02:14:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2017 02:14:00 GMT
EXPOSE 2368/tcp
# Thu, 23 Mar 2017 02:14:01 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c75255d33f781986e7e2731d7b17bf4675d02f4e956371310df4658cf1b1b2`  
		Last Modified: Thu, 23 Mar 2017 00:09:59 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab9991517f0812d77cbf980badfb70ae7fc1d2c7386fcd6237d55f9f39b8897`  
		Last Modified: Thu, 23 Mar 2017 00:35:52 GMT  
		Size: 119.1 KB (119060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d0bbc00fae7c4785fe022064450877586372eb2f1fc5658c84476457ef8c7e`  
		Last Modified: Thu, 23 Mar 2017 00:57:46 GMT  
		Size: 12.2 MB (12246199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984285df6d9ce05e8d5edd2c888482cfddf92ffd1d161a861b65f4d844bc5bd5`  
		Last Modified: Thu, 23 Mar 2017 00:57:41 GMT  
		Size: 875.4 KB (875449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f15ebe0194985f1d3f48d3357b615b7d399ff99d38dc109908e95fba8d5e938`  
		Last Modified: Thu, 23 Mar 2017 02:14:29 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e5a65238497b7e0ffb67e0385858670d474d38e02ca3f88c89186a621bdd9`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 807.9 KB (807936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f977180392de50fe9e298078ea5cd6c6a0f6bb7167956f3171f67a7c1bb5ce6`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f11ba05ac1c0c87d4d155b88f0a45fe906282c2c433b2a60be4f81a7752`  
		Last Modified: Thu, 23 Mar 2017 02:14:41 GMT  
		Size: 27.2 MB (27243404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a28a138fccae7a3f0a4154ade7d79adb30de8ba0bb91f9e423a40bdfd8e9ca5`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f551a294d5b599f9cc335a12cac7751e2df6da026926c2205f6e477fea84edc`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 524.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11`

```console
$ docker pull ghost@sha256:0cf2fdcc10db488992cb764b40009d0da12f2f88957928758c2ca2e7ec94ee26
```

-	Platforms:
	-	linux; amd64

### `ghost:0.11` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111346590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e23922b175cd5ede2ff9539f16372880a857fae79f98480e2313d1f487e08c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:07:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 22 Mar 2017 23:53:28 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Wed, 22 Mar 2017 23:53:45 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 23 Mar 2017 00:28:34 GMT
ENV NODE_VERSION=4.8.1
# Thu, 23 Mar 2017 00:28:46 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 23 Mar 2017 00:28:46 GMT
ENV YARN_VERSION=0.21.3
# Thu, 23 Mar 2017 00:28:51 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done   && curl -fSL -o yarn.js "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js"   && curl -fSL -o yarn.js.asc "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js.asc"   && gpg --batch --verify yarn.js.asc yarn.js   && rm yarn.js.asc   && mv yarn.js /usr/local/bin/yarn   && chmod +x /usr/local/bin/yarn
# Thu, 23 Mar 2017 00:28:51 GMT
CMD ["node"]
# Thu, 23 Mar 2017 02:12:35 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Thu, 23 Mar 2017 02:12:36 GMT
ENV GOSU_VERSION=1.7
# Thu, 23 Mar 2017 02:12:40 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Thu, 23 Mar 2017 02:12:40 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Thu, 23 Mar 2017 02:12:40 GMT
WORKDIR /usr/src/ghost
# Thu, 23 Mar 2017 02:12:41 GMT
ENV GHOST_VERSION=0.11.7
# Thu, 23 Mar 2017 02:13:57 GMT
RUN buildDeps=' 		gcc 		make 		python 		unzip 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip" 	&& unzip ghost.zip 	&& npm install --production 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false $buildDeps 	&& rm ghost.zip 	&& npm cache clean 	&& rm -rf /tmp/npm*
# Thu, 23 Mar 2017 02:13:58 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Thu, 23 Mar 2017 02:13:59 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Thu, 23 Mar 2017 02:13:59 GMT
VOLUME [/var/lib/ghost]
# Thu, 23 Mar 2017 02:14:00 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /entrypoint.sh 
# Thu, 23 Mar 2017 02:14:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2017 02:14:00 GMT
EXPOSE 2368/tcp
# Thu, 23 Mar 2017 02:14:01 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c75255d33f781986e7e2731d7b17bf4675d02f4e956371310df4658cf1b1b2`  
		Last Modified: Thu, 23 Mar 2017 00:09:59 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab9991517f0812d77cbf980badfb70ae7fc1d2c7386fcd6237d55f9f39b8897`  
		Last Modified: Thu, 23 Mar 2017 00:35:52 GMT  
		Size: 119.1 KB (119060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d0bbc00fae7c4785fe022064450877586372eb2f1fc5658c84476457ef8c7e`  
		Last Modified: Thu, 23 Mar 2017 00:57:46 GMT  
		Size: 12.2 MB (12246199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984285df6d9ce05e8d5edd2c888482cfddf92ffd1d161a861b65f4d844bc5bd5`  
		Last Modified: Thu, 23 Mar 2017 00:57:41 GMT  
		Size: 875.4 KB (875449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f15ebe0194985f1d3f48d3357b615b7d399ff99d38dc109908e95fba8d5e938`  
		Last Modified: Thu, 23 Mar 2017 02:14:29 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e5a65238497b7e0ffb67e0385858670d474d38e02ca3f88c89186a621bdd9`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 807.9 KB (807936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f977180392de50fe9e298078ea5cd6c6a0f6bb7167956f3171f67a7c1bb5ce6`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f11ba05ac1c0c87d4d155b88f0a45fe906282c2c433b2a60be4f81a7752`  
		Last Modified: Thu, 23 Mar 2017 02:14:41 GMT  
		Size: 27.2 MB (27243404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a28a138fccae7a3f0a4154ade7d79adb30de8ba0bb91f9e423a40bdfd8e9ca5`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f551a294d5b599f9cc335a12cac7751e2df6da026926c2205f6e477fea84edc`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 524.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0`

```console
$ docker pull ghost@sha256:0cf2fdcc10db488992cb764b40009d0da12f2f88957928758c2ca2e7ec94ee26
```

-	Platforms:
	-	linux; amd64

### `ghost:0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111346590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e23922b175cd5ede2ff9539f16372880a857fae79f98480e2313d1f487e08c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:07:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 22 Mar 2017 23:53:28 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Wed, 22 Mar 2017 23:53:45 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 23 Mar 2017 00:28:34 GMT
ENV NODE_VERSION=4.8.1
# Thu, 23 Mar 2017 00:28:46 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 23 Mar 2017 00:28:46 GMT
ENV YARN_VERSION=0.21.3
# Thu, 23 Mar 2017 00:28:51 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done   && curl -fSL -o yarn.js "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js"   && curl -fSL -o yarn.js.asc "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js.asc"   && gpg --batch --verify yarn.js.asc yarn.js   && rm yarn.js.asc   && mv yarn.js /usr/local/bin/yarn   && chmod +x /usr/local/bin/yarn
# Thu, 23 Mar 2017 00:28:51 GMT
CMD ["node"]
# Thu, 23 Mar 2017 02:12:35 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Thu, 23 Mar 2017 02:12:36 GMT
ENV GOSU_VERSION=1.7
# Thu, 23 Mar 2017 02:12:40 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Thu, 23 Mar 2017 02:12:40 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Thu, 23 Mar 2017 02:12:40 GMT
WORKDIR /usr/src/ghost
# Thu, 23 Mar 2017 02:12:41 GMT
ENV GHOST_VERSION=0.11.7
# Thu, 23 Mar 2017 02:13:57 GMT
RUN buildDeps=' 		gcc 		make 		python 		unzip 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip" 	&& unzip ghost.zip 	&& npm install --production 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false $buildDeps 	&& rm ghost.zip 	&& npm cache clean 	&& rm -rf /tmp/npm*
# Thu, 23 Mar 2017 02:13:58 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Thu, 23 Mar 2017 02:13:59 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Thu, 23 Mar 2017 02:13:59 GMT
VOLUME [/var/lib/ghost]
# Thu, 23 Mar 2017 02:14:00 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /entrypoint.sh 
# Thu, 23 Mar 2017 02:14:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2017 02:14:00 GMT
EXPOSE 2368/tcp
# Thu, 23 Mar 2017 02:14:01 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c75255d33f781986e7e2731d7b17bf4675d02f4e956371310df4658cf1b1b2`  
		Last Modified: Thu, 23 Mar 2017 00:09:59 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab9991517f0812d77cbf980badfb70ae7fc1d2c7386fcd6237d55f9f39b8897`  
		Last Modified: Thu, 23 Mar 2017 00:35:52 GMT  
		Size: 119.1 KB (119060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d0bbc00fae7c4785fe022064450877586372eb2f1fc5658c84476457ef8c7e`  
		Last Modified: Thu, 23 Mar 2017 00:57:46 GMT  
		Size: 12.2 MB (12246199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984285df6d9ce05e8d5edd2c888482cfddf92ffd1d161a861b65f4d844bc5bd5`  
		Last Modified: Thu, 23 Mar 2017 00:57:41 GMT  
		Size: 875.4 KB (875449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f15ebe0194985f1d3f48d3357b615b7d399ff99d38dc109908e95fba8d5e938`  
		Last Modified: Thu, 23 Mar 2017 02:14:29 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e5a65238497b7e0ffb67e0385858670d474d38e02ca3f88c89186a621bdd9`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 807.9 KB (807936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f977180392de50fe9e298078ea5cd6c6a0f6bb7167956f3171f67a7c1bb5ce6`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f11ba05ac1c0c87d4d155b88f0a45fe906282c2c433b2a60be4f81a7752`  
		Last Modified: Thu, 23 Mar 2017 02:14:41 GMT  
		Size: 27.2 MB (27243404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a28a138fccae7a3f0a4154ade7d79adb30de8ba0bb91f9e423a40bdfd8e9ca5`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f551a294d5b599f9cc335a12cac7751e2df6da026926c2205f6e477fea84edc`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 524.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:0cf2fdcc10db488992cb764b40009d0da12f2f88957928758c2ca2e7ec94ee26
```

-	Platforms:
	-	linux; amd64

### `ghost:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111346590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e23922b175cd5ede2ff9539f16372880a857fae79f98480e2313d1f487e08c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 22:07:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 22 Mar 2017 23:53:28 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Wed, 22 Mar 2017 23:53:45 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Thu, 23 Mar 2017 00:28:34 GMT
ENV NODE_VERSION=4.8.1
# Thu, 23 Mar 2017 00:28:46 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 23 Mar 2017 00:28:46 GMT
ENV YARN_VERSION=0.21.3
# Thu, 23 Mar 2017 00:28:51 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done   && curl -fSL -o yarn.js "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js"   && curl -fSL -o yarn.js.asc "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js.asc"   && gpg --batch --verify yarn.js.asc yarn.js   && rm yarn.js.asc   && mv yarn.js /usr/local/bin/yarn   && chmod +x /usr/local/bin/yarn
# Thu, 23 Mar 2017 00:28:51 GMT
CMD ["node"]
# Thu, 23 Mar 2017 02:12:35 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Thu, 23 Mar 2017 02:12:36 GMT
ENV GOSU_VERSION=1.7
# Thu, 23 Mar 2017 02:12:40 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Thu, 23 Mar 2017 02:12:40 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Thu, 23 Mar 2017 02:12:40 GMT
WORKDIR /usr/src/ghost
# Thu, 23 Mar 2017 02:12:41 GMT
ENV GHOST_VERSION=0.11.7
# Thu, 23 Mar 2017 02:13:57 GMT
RUN buildDeps=' 		gcc 		make 		python 		unzip 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip" 	&& unzip ghost.zip 	&& npm install --production 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false -o APT::AutoRemove::SuggestsImportant=false $buildDeps 	&& rm ghost.zip 	&& npm cache clean 	&& rm -rf /tmp/npm*
# Thu, 23 Mar 2017 02:13:58 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Thu, 23 Mar 2017 02:13:59 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Thu, 23 Mar 2017 02:13:59 GMT
VOLUME [/var/lib/ghost]
# Thu, 23 Mar 2017 02:14:00 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /entrypoint.sh 
# Thu, 23 Mar 2017 02:14:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2017 02:14:00 GMT
EXPOSE 2368/tcp
# Thu, 23 Mar 2017 02:14:01 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c75255d33f781986e7e2731d7b17bf4675d02f4e956371310df4658cf1b1b2`  
		Last Modified: Thu, 23 Mar 2017 00:09:59 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab9991517f0812d77cbf980badfb70ae7fc1d2c7386fcd6237d55f9f39b8897`  
		Last Modified: Thu, 23 Mar 2017 00:35:52 GMT  
		Size: 119.1 KB (119060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d0bbc00fae7c4785fe022064450877586372eb2f1fc5658c84476457ef8c7e`  
		Last Modified: Thu, 23 Mar 2017 00:57:46 GMT  
		Size: 12.2 MB (12246199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984285df6d9ce05e8d5edd2c888482cfddf92ffd1d161a861b65f4d844bc5bd5`  
		Last Modified: Thu, 23 Mar 2017 00:57:41 GMT  
		Size: 875.4 KB (875449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f15ebe0194985f1d3f48d3357b615b7d399ff99d38dc109908e95fba8d5e938`  
		Last Modified: Thu, 23 Mar 2017 02:14:29 GMT  
		Size: 4.4 KB (4378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e5a65238497b7e0ffb67e0385858670d474d38e02ca3f88c89186a621bdd9`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 807.9 KB (807936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f977180392de50fe9e298078ea5cd6c6a0f6bb7167956f3171f67a7c1bb5ce6`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f11ba05ac1c0c87d4d155b88f0a45fe906282c2c433b2a60be4f81a7752`  
		Last Modified: Thu, 23 Mar 2017 02:14:41 GMT  
		Size: 27.2 MB (27243404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a28a138fccae7a3f0a4154ade7d79adb30de8ba0bb91f9e423a40bdfd8e9ca5`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f551a294d5b599f9cc335a12cac7751e2df6da026926c2205f6e477fea84edc`  
		Last Modified: Thu, 23 Mar 2017 02:14:26 GMT  
		Size: 524.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
