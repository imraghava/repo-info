## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:070d5ae011e52315a3a92528e75c61a6931baad4ec4525966e06740e6dce43e9
```

-	Platforms:
	-	windows; amd64

### `golang:1-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5368679492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b648944b381b9d1f7c05ab2b6a8d1017880df5f9aa1e774d7a5d549c1b1c263`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 22 Nov 2016 23:24:24 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Apr 2017 22:00:56 GMT
RUN Install update 10.0.14393.1066
# Wed, 26 Apr 2017 19:30:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Apr 2017 19:30:54 GMT
ENV GIT_VERSION=2.11.1
# Wed, 26 Apr 2017 19:30:56 GMT
ENV GIT_TAG=v2.11.1.windows.1
# Wed, 26 Apr 2017 19:30:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.11.1.windows.1/MinGit-2.11.1-64-bit.zip
# Wed, 26 Apr 2017 19:31:01 GMT
ENV GIT_DOWNLOAD_SHA256=668d16a799dd721ed126cc91bed49eb2c072ba1b25b50048280a4e2c5ed56e59
# Wed, 26 Apr 2017 19:32:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  git --version'; git --version; 		Write-Host 'Complete.';
# Wed, 26 Apr 2017 19:32:23 GMT
ENV GOPATH=C:\gopath
# Wed, 26 Apr 2017 19:33:08 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 May 2017 23:16:09 GMT
ENV GOLANG_VERSION=1.8.3
# Wed, 24 May 2017 23:19:03 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'de026caef4c5b4a74f359737dcb2d14c67ca45c45093755d3b0d2e0ee3aafd96'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Wed, 24 May 2017 23:19:07 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d4d50238ed13902c153bc3efc3a22f8a96bca4168ea03624d01da1063728dc2`  
		Size: 1.2 GB (1161902022 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1363e862fdfb51b375f642fff311ab5f16a4e990d8d8c0ef1a0c9b563692b9ff`  
		Last Modified: Wed, 26 Apr 2017 19:51:11 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d158fdba2085467b086532bdef037f6c3e01a8e4c98b6038fb14e6676a0797da`  
		Last Modified: Wed, 26 Apr 2017 19:51:11 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb15d8910eb9c1eacc4caa25f5c9b435980b9e21a1b444642cf0fc531ef4256`  
		Last Modified: Wed, 26 Apr 2017 19:51:09 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47849740fa1bc93b5e949cc3a162272b1bc0195e36f3c1e58ef9f2a5d00bb4be`  
		Last Modified: Wed, 26 Apr 2017 19:51:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4468c50bc88aca6818d8e8de7227c48675cac2973b7809d96c2013e35a115967`  
		Last Modified: Wed, 26 Apr 2017 19:51:04 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bdc1f87b8a2c0ca9fb770410e3ffbf0ab24ac237237b9ea14fec80afd3dd5b`  
		Last Modified: Wed, 26 Apr 2017 19:51:18 GMT  
		Size: 29.4 MB (29367839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d90260aa9b0d30a56d43412e6a7b83fa5c64125602737360844aaf02dbbb64`  
		Last Modified: Wed, 26 Apr 2017 19:50:58 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b711361369e4436d130eeedbec0cb505eba3f1306c48e03ffde37521925e98`  
		Last Modified: Wed, 26 Apr 2017 19:51:01 GMT  
		Size: 4.7 MB (4664221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b331d15aa621885c086c370b0acd3f098bb7061187021ec2f4042218deb2ff1`  
		Last Modified: Wed, 24 May 2017 23:22:11 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c632a99d7492e69b58a43144c119720fdd94bb23e568ad093cb2a701c88a3d2`  
		Last Modified: Wed, 24 May 2017 23:22:32 GMT  
		Size: 102.7 MB (102749745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476df5a9b09e1b23f2d2d3db74cbbc07083f6d83e6678edc6299d22f6a9040d`  
		Last Modified: Wed, 24 May 2017 23:22:10 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
