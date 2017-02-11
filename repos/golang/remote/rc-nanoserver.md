## `golang:rc-nanoserver`

```console
$ docker pull golang@sha256:e95544578ee816c0481b30c6dbc5a224039694de5b19e1c84387ed3033b3afdd
```

-	Platforms:
	-	windows; amd64

### `golang:rc-nanoserver` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.5 MB (427508952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8345fdae32a09bbeb6eb4eef04a5f520d515385e04506c105f9562a700f992e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 13 Jan 2017 17:53:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Jan 2017 17:53:31 GMT
ENV GOPATH=C:\gopath
# Fri, 13 Jan 2017 17:54:11 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Fri, 10 Feb 2017 00:24:12 GMT
ENV GOLANG_VERSION=1.8rc3
# Fri, 10 Feb 2017 00:24:14 GMT
ENV GOLANG_DOWNLOAD_URL=https://golang.org/dl/go1.8rc3.windows-amd64.zip
# Fri, 10 Feb 2017 00:24:16 GMT
ENV GOLANG_DOWNLOAD_SHA256=9ac7224a79dfd2d390ff4c5202f09fae2a5b07e9b0ebf32913979635e7143383
# Fri, 10 Feb 2017 00:27:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GOLANG_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GOLANG_DOWNLOAD_URL -OutFile 'go.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GOLANG_DOWNLOAD_SHA256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $env:GOLANG_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Fri, 10 Feb 2017 00:27:50 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ac17e2e6106d09a44642a437c318092eddd284afea0b4e707e89f6cec7a18ef`  
		Size: 80.6 MB (80617684 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e75762e22d922ed4bb69ae4e673c912389d9d70fd91eaa33cd0732f0a8e28a4e`  
		Last Modified: Fri, 13 Jan 2017 18:00:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110ea2ec6249baec774cf0bb6d4c46f383320ec4ad5e0a72597d9c1ef1834b32`  
		Last Modified: Fri, 13 Jan 2017 18:00:04 GMT  
		Size: 967.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15068a1a55e80e8468c9cd1bfd0c5b53faf86bd29b5b2a6692b41986129b29a8`  
		Last Modified: Fri, 13 Jan 2017 18:00:08 GMT  
		Size: 865.5 KB (865469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedd1e8252608ae6c5f9002e5de0506da991e30a29afd1e51e6be417f48bbc85`  
		Last Modified: Fri, 10 Feb 2017 00:30:20 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3accb584a71c186dd14ab2c14523222efb87276aa3a7a335ac3274ad4d88698d`  
		Last Modified: Fri, 10 Feb 2017 00:30:20 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b9b38f4151bbce0b92987c522ec6519ce025445d21f071b926632a6b657458`  
		Last Modified: Fri, 10 Feb 2017 00:30:19 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c32a3a77d3511589b1c2ca4efd765694b94fb78f0db750c66f2eafe17ae519`  
		Last Modified: Fri, 10 Feb 2017 00:30:45 GMT  
		Size: 93.3 MB (93329064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ff02147674081174b08a2e7775a3a999cc1f00813078deb03572cca9c1b33b`  
		Last Modified: Fri, 10 Feb 2017 00:30:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip