## `golang:windowsservercore`

```console
$ docker pull golang@sha256:4714b98b1d9cace1cab73dc8b4fc008884ff76085d15c5e264510e36c6d5118b
```

-	Platforms:
	-	windows; amd64

### `golang:windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 GB (5126343607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de920b72f3979e7cd4517dcf3c76531e7fca6536e72fe5ee47a55fd2c58bde0c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 18 Jan 2017 00:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Feb 2017 20:27:19 GMT
ENV GIT_VERSION=2.11.1
# Wed, 15 Feb 2017 20:27:22 GMT
ENV GIT_TAG=v2.11.1.windows.1
# Wed, 15 Feb 2017 20:27:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.11.1.windows.1/MinGit-2.11.1-64-bit.zip
# Wed, 15 Feb 2017 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=668d16a799dd721ed126cc91bed49eb2c072ba1b25b50048280a4e2c5ed56e59
# Wed, 15 Feb 2017 20:28:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  git --version'; git --version; 		Write-Host 'Complete.';
# Wed, 15 Feb 2017 20:28:09 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Feb 2017 20:28:30 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2017 23:21:10 GMT
ENV GOLANG_VERSION=1.8
# Thu, 16 Feb 2017 23:21:13 GMT
ENV GOLANG_DOWNLOAD_URL=https://golang.org/dl/go1.8.windows-amd64.zip
# Thu, 16 Feb 2017 23:21:16 GMT
ENV GOLANG_DOWNLOAD_SHA256=cb27fe210f3a9d10329d48514895d2a1e3651125a7c3c758f0358a5bfc0e3060
# Thu, 16 Feb 2017 23:25:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GOLANG_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GOLANG_DOWNLOAD_URL -OutFile 'go.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GOLANG_DOWNLOAD_SHA256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $env:GOLANG_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Thu, 16 Feb 2017 23:25:19 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3430754e4d171ead00cf6766797a28abf3caf236f6c92c5c346ea2ad3955a129`  
		Size: 913.1 MB (913145061 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2090e83c9aacacb2da7d0836cf297e9927a3137c208e2f631e39e181e31ceb90`  
		Last Modified: Wed, 18 Jan 2017 22:56:55 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6257b3811def44ee6b788cc3f855820ccf44038641d8d8ad23dac1accc4760`  
		Last Modified: Wed, 15 Feb 2017 20:40:33 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb455a144c287f63ab88e55546f753cb4454f5a3e85b0d52a65b0b206aebc2e`  
		Last Modified: Wed, 15 Feb 2017 20:40:31 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c3d32c5bd38ab16138f5b6bf6cea5bcd0aa67824aceb075840739de217de1b`  
		Last Modified: Wed, 15 Feb 2017 20:40:30 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edfd99f5adb5dec83cf253725121285d8e425b9be2ef09ebbd9e248e0fce19`  
		Last Modified: Wed, 15 Feb 2017 20:40:26 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d539344b85c3378e0a8c90f0671a0e8b1691cf0dc196e0fe486932f4730d3eb`  
		Last Modified: Wed, 15 Feb 2017 20:40:42 GMT  
		Size: 33.6 MB (33587430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c72df54202f58a190e11d26d1c905e6bedd08cdf2f1828cc177fba0605842e`  
		Last Modified: Wed, 15 Feb 2017 20:40:25 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01c980f6e1f89dcdfb186c88eae59f0f6cd8c8b9c9b6819cdb460f8ac39c98a`  
		Last Modified: Wed, 15 Feb 2017 20:40:27 GMT  
		Size: 8.0 MB (7970960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207c0640cc8594c733b8c979642f737033ff1e97a98c6b5526d165345794897f`  
		Last Modified: Thu, 16 Feb 2017 23:29:37 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54176c15eddbdec0401a7698304db2fc41d2daabde37352b67732f7308d2facc`  
		Last Modified: Thu, 16 Feb 2017 23:29:38 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0683f52848a04d4b07cb327896a85c8bca33acf4b1af99b3c68474753d33bd4e`  
		Last Modified: Thu, 16 Feb 2017 23:29:37 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1773ae09eefeebec3baafc00b839a2329437955a0f393fad847a36fbfe8b23`  
		Last Modified: Thu, 16 Feb 2017 23:29:58 GMT  
		Size: 101.6 MB (101642015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071401ef7de6d962ecb05d63e0e2b55a82de0b5f87a96f47a4940c8098507fa1`  
		Last Modified: Thu, 16 Feb 2017 23:29:37 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
