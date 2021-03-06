## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:a15a12787f73c4d478beaf8277b1c6de27c511abb6f8e7d85c8ca5e03aa603d3
```

-	Platforms:
	-	linux; amd64

### `eggdrop:stable` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d76cc57d1277f8a0371b7fd6ef9ccfaca635ec56848b3ac1b1e155c4f3f611`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 21:48:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 03 Mar 2017 21:48:51 GMT
RUN adduser -S eggdrop
# Fri, 03 Mar 2017 21:48:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 03 Mar 2017 21:49:58 GMT
RUN apk add --no-cache tcl tcl-dev wget ca-certificates make tar gpgme bash build-base openssl openssl-dev  && wget ftp://ftp.eggheads.org/pub/eggdrop/source/stable/eggdrop-1.8.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/stable/eggdrop-1.8.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.0.tar.gz.asc eggdrop-1.8.0.tar.gz   && rm eggdrop-1.8.0.tar.gz.asc   && tar -zxvf eggdrop-1.8.0.tar.gz   && rm eggdrop-1.8.0.tar.gz   && ( cd eggdrop-1.8.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev
# Fri, 03 Mar 2017 21:49:59 GMT
ENV NICK=
# Fri, 03 Mar 2017 21:49:59 GMT
ENV SERVER=
# Fri, 03 Mar 2017 21:49:59 GMT
ENV LISTEN=3333
# Fri, 03 Mar 2017 21:50:00 GMT
ENV OWNER=
# Fri, 03 Mar 2017 21:50:00 GMT
ENV USERFILE=eggdrop.user
# Fri, 03 Mar 2017 21:50:00 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 03 Mar 2017 21:50:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 03 Mar 2017 21:50:01 GMT
EXPOSE 3333/tcp
# Fri, 03 Mar 2017 21:50:01 GMT
COPY file:7a054cb46364a47f244469cd44e0d12e9e0c49ab06cd99348b2a2bba3a4fb1c8 in /home/eggdrop/eggdrop 
# Fri, 03 Mar 2017 21:50:02 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Fri, 03 Mar 2017 21:50:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 03 Mar 2017 21:50:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc5c47fff02df2b35ae358a2202af4e17996168dc37b707a35cf0dd467f3734`  
		Last Modified: Sat, 04 Mar 2017 04:51:19 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90e3857bd72846a4c81f7ed61db77dc8cc8462fa581cd45ab69ec251efd85cc`  
		Last Modified: Sat, 04 Mar 2017 04:51:19 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1216bb5acbef1b631d01e5e8d66c10a49054ad0674a26621274e2be08a31fb5`  
		Last Modified: Sat, 04 Mar 2017 04:52:06 GMT  
		Size: 5.0 MB (5041986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6f1d66c41405eb53ef8e367131a8096fb922f8820302ccab37faa0b65e581b`  
		Last Modified: Sat, 04 Mar 2017 04:52:02 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4fe58132d241b1bc965daefb91f058d5a2c0d6b6da6c0e507a15cbb8bd108a`  
		Last Modified: Sat, 04 Mar 2017 04:52:01 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
