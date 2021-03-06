## `jenkins:alpine`

```console
$ docker pull jenkins@sha256:905b236c83bef3bfddf4ab5fbe32f49bdd1362f96d3aad5a5ba1e32b431d08f4
```

-	Platforms:
	-	linux; amd64

### `jenkins:alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166062515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf98efaba71ce74dcaea15cb28b5ef4abe07d99ef9c7106d66e2e9e65a9a5b8f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/jenkins.sh"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Tue, 07 Mar 2017 01:03:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Mar 2017 01:03:59 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 07 Mar 2017 01:04:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Tue, 07 Mar 2017 01:04:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 07 Mar 2017 01:04:01 GMT
ENV JAVA_VERSION=8u121
# Tue, 07 Mar 2017 01:04:01 GMT
ENV JAVA_ALPINE_VERSION=8.121.13-r0
# Tue, 07 Mar 2017 01:04:07 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 07 Mar 2017 18:30:06 GMT
RUN apk add --no-cache git openssh-client curl unzip bash ttf-dejavu coreutils
# Tue, 07 Mar 2017 18:30:07 GMT
ENV JENKINS_HOME=/var/jenkins_home
# Tue, 07 Mar 2017 18:30:08 GMT
ENV JENKINS_SLAVE_AGENT_PORT=50000
# Tue, 07 Mar 2017 18:30:08 GMT
ARG user=jenkins
# Tue, 07 Mar 2017 18:30:09 GMT
ARG group=jenkins
# Tue, 07 Mar 2017 18:30:10 GMT
ARG uid=1000
# Tue, 07 Mar 2017 18:30:10 GMT
ARG gid=1000
# Tue, 07 Mar 2017 18:30:12 GMT
# ARGS: gid=1000 group=jenkins uid=1000 user=jenkins
RUN addgroup -g ${gid} ${group}     && adduser -h "$JENKINS_HOME" -u ${uid} -G ${group} -s /bin/bash -D ${user}
# Tue, 07 Mar 2017 18:30:12 GMT
VOLUME [/var/jenkins_home]
# Tue, 07 Mar 2017 18:30:13 GMT
# ARGS: gid=1000 group=jenkins uid=1000 user=jenkins
RUN mkdir -p /usr/share/jenkins/ref/init.groovy.d
# Tue, 07 Mar 2017 18:30:14 GMT
ENV TINI_VERSION=0.13.2
# Tue, 07 Mar 2017 18:30:15 GMT
ENV TINI_SHA=afbf8de8a63ce8e4f18cb3f34dfdbbd354af68a1
# Tue, 07 Mar 2017 18:30:17 GMT
# ARGS: gid=1000 group=jenkins uid=1000 user=jenkins
RUN curl -fsSL https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-static-amd64 -o /bin/tini && chmod +x /bin/tini   && echo "$TINI_SHA  /bin/tini" | sha1sum -c -
# Tue, 07 Mar 2017 18:30:18 GMT
COPY file:c629bc0b9ecb5b7233000c973f65721df4ce1307a5d5b33ac3871ff61a9172ff in /usr/share/jenkins/ref/init.groovy.d/tcp-slave-agent-port.groovy 
# Tue, 07 Mar 2017 18:30:19 GMT
ARG JENKINS_VERSION
# Tue, 07 Mar 2017 18:30:19 GMT
ENV JENKINS_VERSION=2.32.3
# Tue, 07 Mar 2017 18:30:20 GMT
ARG JENKINS_SHA=a25b9a314ca9e76f9673da7309e1882e32674223
# Tue, 07 Mar 2017 18:30:21 GMT
ARG JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.32.3/jenkins-war-2.32.3.war
# Tue, 07 Mar 2017 18:30:25 GMT
# ARGS: JENKINS_SHA=a25b9a314ca9e76f9673da7309e1882e32674223 JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.32.3/jenkins-war-2.32.3.war gid=1000 group=jenkins uid=1000 user=jenkins
RUN curl -fsSL ${JENKINS_URL} -o /usr/share/jenkins/jenkins.war   && echo "${JENKINS_SHA}  /usr/share/jenkins/jenkins.war" | sha1sum -c -
# Tue, 07 Mar 2017 18:30:26 GMT
ENV JENKINS_UC=https://updates.jenkins.io
# Tue, 07 Mar 2017 18:30:27 GMT
# ARGS: JENKINS_SHA=a25b9a314ca9e76f9673da7309e1882e32674223 JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.32.3/jenkins-war-2.32.3.war gid=1000 group=jenkins uid=1000 user=jenkins
RUN chown -R ${user} "$JENKINS_HOME" /usr/share/jenkins/ref
# Tue, 07 Mar 2017 18:30:28 GMT
EXPOSE 8080/tcp
# Tue, 07 Mar 2017 18:30:28 GMT
EXPOSE 50000/tcp
# Tue, 07 Mar 2017 18:30:29 GMT
ENV COPY_REFERENCE_FILE_LOG=/var/jenkins_home/copy_reference_file.log
# Tue, 07 Mar 2017 18:30:29 GMT
USER [jenkins]
# Tue, 07 Mar 2017 18:30:30 GMT
COPY file:26c3c5818bc87662d1f4905a3ed73bd55a0a75f731c7dc52d0599c00f51408e9 in /usr/local/bin/jenkins-support 
# Tue, 07 Mar 2017 18:30:31 GMT
COPY file:7eec179a0dd3aad4a9c9290bc4d85e4775c8cf6bc2932527892ca6e87739e474 in /usr/local/bin/jenkins.sh 
# Tue, 07 Mar 2017 18:30:32 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/jenkins.sh"]
# Tue, 07 Mar 2017 18:30:33 GMT
COPY file:93fb511d485dd2d6060c484dcedb902947875042048de529676a0a0aed27b5a3 in /usr/local/bin/plugins.sh 
# Tue, 07 Mar 2017 18:30:34 GMT
COPY file:2a6a3e16202b8dddab5edef50f712c16fe8f6980f5aea80c8c76b5db4f903913 in /usr/local/bin/install-plugins.sh 
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de20f2d8b839756d5fc0ae6871096666a822b6b4205e11e9cf438a2263f3281`  
		Last Modified: Tue, 07 Mar 2017 01:12:49 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e00029ebfe30f96f53c89cd3c838b89876ee212cbb545e8ac5c70698c1818f1`  
		Last Modified: Tue, 07 Mar 2017 01:12:59 GMT  
		Size: 69.6 MB (69564916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1839d7896efa48fb1945d2f1bbd58124ca9bb796536442ee631733c0f2c0298b`  
		Last Modified: Tue, 07 Mar 2017 18:31:05 GMT  
		Size: 24.6 MB (24575751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750cfd608edc68af55e0dc5130f9e4113d6ab1b48c7d0dbc0987f7f44cf1bd39`  
		Last Modified: Tue, 07 Mar 2017 18:30:57 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235d8aedfa97c29f7b116a9505b040f623d1199641b07ea38aa2e1f222c8b9a6`  
		Last Modified: Tue, 07 Mar 2017 18:30:57 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a93da4c692e7766d3c29a90682af47b5b39ad5021802a84c65297684a1915d`  
		Last Modified: Tue, 07 Mar 2017 18:30:57 GMT  
		Size: 344.9 KB (344859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be93cb336ed7485319935f90f66f66146104caf99ceaaa9d5bf48f566a524a1e`  
		Last Modified: Tue, 07 Mar 2017 18:30:56 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2627b3478cf400da8bc57e8084eb51391b357f60f2f88cdfcd5a6f38cccb8431`  
		Last Modified: Tue, 07 Mar 2017 18:31:01 GMT  
		Size: 69.7 MB (69663297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0a918969e088df1e10ca533097b59f9234a6e4e1aff3a4102c20324c20afe`  
		Last Modified: Tue, 07 Mar 2017 18:30:54 GMT  
		Size: 426.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f0989d3476b9bf969b782826773f6d072b1f84b24fac06ce3e38e2813ca717`  
		Last Modified: Tue, 07 Mar 2017 18:30:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebff3be068fd9e76b902a01abe418f3020dfa683160134141871df7bfe63235`  
		Last Modified: Tue, 07 Mar 2017 18:30:54 GMT  
		Size: 813.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d80188d4e13093eeb2134a063042ad8880eb4ca69fb8ab8ef527b52088f125`  
		Last Modified: Tue, 07 Mar 2017 18:30:54 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e367ea4282535417f004fb50dad4d539f3c399e1d1a7c427112e9de6c0fb22`  
		Last Modified: Tue, 07 Mar 2017 18:30:54 GMT  
		Size: 2.2 KB (2172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
