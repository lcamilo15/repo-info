<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rocket.chat`

-	[`rocket.chat:0.54.0`](#rocketchat0540)
-	[`rocket.chat:0.54`](#rocketchat054)
-	[`rocket.chat:0`](#rocketchat0)
-	[`rocket.chat:latest`](#rocketchatlatest)

## `rocket.chat:0.54.0`

```console
$ docker pull rocket.chat@sha256:3aecaf113f9af497e1c4e74ebe1a44de4ba13f17e7f423f868e64ffdb6d4053c
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:0.54.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (179951617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f809c5ec2423f8a0c520b98899621136b89ff165f5469bbcbf5437c97b82a58`
-	Default Command: `["node","main.js"]`

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
# Thu, 23 Mar 2017 02:18:17 GMT
MAINTAINER buildmaster@rocket.chat
# Thu, 23 Mar 2017 02:18:19 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat
# Thu, 23 Mar 2017 02:18:19 GMT
VOLUME [/app/uploads]
# Thu, 23 Mar 2017 02:18:39 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Thu, 23 Mar 2017 02:18:40 GMT
ENV RC_VERSION=0.54.0
# Thu, 23 Mar 2017 02:18:42 GMT
WORKDIR /app
# Thu, 23 Mar 2017 02:20:35 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Thu, 23 Mar 2017 02:31:28 GMT
USER [rocketchat]
# Thu, 23 Mar 2017 02:31:28 GMT
WORKDIR /app/bundle
# Thu, 23 Mar 2017 02:31:29 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 23 Mar 2017 02:31:30 GMT
EXPOSE 3000/tcp
# Thu, 23 Mar 2017 02:31:30 GMT
CMD ["node" "main.js"]
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
	-	`sha256:6f5cff59c097b75a69df8641925b9f9db37eb78929ddd7fdebd93780363851f3`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0dca16f54d9a7899f5379fe54966bd122cbd59ab0f6c7bb74a9db9a7f33f4e`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 127.3 KB (127265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fcf5f9158c4d1564641fec5e4ff3de81d06264171e139d616496df4296923`  
		Last Modified: Thu, 23 Mar 2017 02:33:29 GMT  
		Size: 96.5 MB (96532256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:0.54`

```console
$ docker pull rocket.chat@sha256:3aecaf113f9af497e1c4e74ebe1a44de4ba13f17e7f423f868e64ffdb6d4053c
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:0.54` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (179951617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f809c5ec2423f8a0c520b98899621136b89ff165f5469bbcbf5437c97b82a58`
-	Default Command: `["node","main.js"]`

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
# Thu, 23 Mar 2017 02:18:17 GMT
MAINTAINER buildmaster@rocket.chat
# Thu, 23 Mar 2017 02:18:19 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat
# Thu, 23 Mar 2017 02:18:19 GMT
VOLUME [/app/uploads]
# Thu, 23 Mar 2017 02:18:39 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Thu, 23 Mar 2017 02:18:40 GMT
ENV RC_VERSION=0.54.0
# Thu, 23 Mar 2017 02:18:42 GMT
WORKDIR /app
# Thu, 23 Mar 2017 02:20:35 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Thu, 23 Mar 2017 02:31:28 GMT
USER [rocketchat]
# Thu, 23 Mar 2017 02:31:28 GMT
WORKDIR /app/bundle
# Thu, 23 Mar 2017 02:31:29 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 23 Mar 2017 02:31:30 GMT
EXPOSE 3000/tcp
# Thu, 23 Mar 2017 02:31:30 GMT
CMD ["node" "main.js"]
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
	-	`sha256:6f5cff59c097b75a69df8641925b9f9db37eb78929ddd7fdebd93780363851f3`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0dca16f54d9a7899f5379fe54966bd122cbd59ab0f6c7bb74a9db9a7f33f4e`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 127.3 KB (127265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fcf5f9158c4d1564641fec5e4ff3de81d06264171e139d616496df4296923`  
		Last Modified: Thu, 23 Mar 2017 02:33:29 GMT  
		Size: 96.5 MB (96532256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:0`

```console
$ docker pull rocket.chat@sha256:3aecaf113f9af497e1c4e74ebe1a44de4ba13f17e7f423f868e64ffdb6d4053c
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (179951617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f809c5ec2423f8a0c520b98899621136b89ff165f5469bbcbf5437c97b82a58`
-	Default Command: `["node","main.js"]`

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
# Thu, 23 Mar 2017 02:18:17 GMT
MAINTAINER buildmaster@rocket.chat
# Thu, 23 Mar 2017 02:18:19 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat
# Thu, 23 Mar 2017 02:18:19 GMT
VOLUME [/app/uploads]
# Thu, 23 Mar 2017 02:18:39 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Thu, 23 Mar 2017 02:18:40 GMT
ENV RC_VERSION=0.54.0
# Thu, 23 Mar 2017 02:18:42 GMT
WORKDIR /app
# Thu, 23 Mar 2017 02:20:35 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Thu, 23 Mar 2017 02:31:28 GMT
USER [rocketchat]
# Thu, 23 Mar 2017 02:31:28 GMT
WORKDIR /app/bundle
# Thu, 23 Mar 2017 02:31:29 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 23 Mar 2017 02:31:30 GMT
EXPOSE 3000/tcp
# Thu, 23 Mar 2017 02:31:30 GMT
CMD ["node" "main.js"]
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
	-	`sha256:6f5cff59c097b75a69df8641925b9f9db37eb78929ddd7fdebd93780363851f3`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0dca16f54d9a7899f5379fe54966bd122cbd59ab0f6c7bb74a9db9a7f33f4e`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 127.3 KB (127265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fcf5f9158c4d1564641fec5e4ff3de81d06264171e139d616496df4296923`  
		Last Modified: Thu, 23 Mar 2017 02:33:29 GMT  
		Size: 96.5 MB (96532256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:3aecaf113f9af497e1c4e74ebe1a44de4ba13f17e7f423f868e64ffdb6d4053c
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (179951617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f809c5ec2423f8a0c520b98899621136b89ff165f5469bbcbf5437c97b82a58`
-	Default Command: `["node","main.js"]`

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
# Thu, 23 Mar 2017 02:18:17 GMT
MAINTAINER buildmaster@rocket.chat
# Thu, 23 Mar 2017 02:18:19 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat
# Thu, 23 Mar 2017 02:18:19 GMT
VOLUME [/app/uploads]
# Thu, 23 Mar 2017 02:18:39 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Thu, 23 Mar 2017 02:18:40 GMT
ENV RC_VERSION=0.54.0
# Thu, 23 Mar 2017 02:18:42 GMT
WORKDIR /app
# Thu, 23 Mar 2017 02:20:35 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Thu, 23 Mar 2017 02:31:28 GMT
USER [rocketchat]
# Thu, 23 Mar 2017 02:31:28 GMT
WORKDIR /app/bundle
# Thu, 23 Mar 2017 02:31:29 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 23 Mar 2017 02:31:30 GMT
EXPOSE 3000/tcp
# Thu, 23 Mar 2017 02:31:30 GMT
CMD ["node" "main.js"]
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
	-	`sha256:6f5cff59c097b75a69df8641925b9f9db37eb78929ddd7fdebd93780363851f3`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0dca16f54d9a7899f5379fe54966bd122cbd59ab0f6c7bb74a9db9a7f33f4e`  
		Last Modified: Thu, 23 Mar 2017 02:31:31 GMT  
		Size: 127.3 KB (127265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675fcf5f9158c4d1564641fec5e4ff3de81d06264171e139d616496df4296923`  
		Last Modified: Thu, 23 Mar 2017 02:33:29 GMT  
		Size: 96.5 MB (96532256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
