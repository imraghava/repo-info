## `nats:nanoserver`

```console
$ docker pull nats@sha256:a41a406be1d24833447caf706a3fc1ea9efae963154065c147b3c7a64c83ea9c
```

-	Platforms:
	-	windows; amd64

### `nats:nanoserver` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371753402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23f257a1b1d6b6dfdbf8b91ed2552709e22044d19bc9a8f863ba914eaf57dc9`
-	Entrypoint: `["gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 20 Nov 2016 11:39:18 GMT
RUN Apply image 10.0.14393.0
# Fri, 07 Apr 2017 09:40:17 GMT
RUN Install update 10.0.14393.1066
# Wed, 26 Apr 2017 19:37:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jul 2017 18:22:08 GMT
ENV NATS_VERSION=v1.0.0
# Wed, 12 Jul 2017 18:22:27 GMT
RUN Invoke-WebRequest -OutFile gnatsd.zip "https://github.com/nats-io/gnatsd/releases/download/$($env:NATS_VERSION)/gnatsd-$($env:NATS_VERSION)-windows-amd64.zip" -UseBasicParsing ;     Expand-Archive gnatsd.zip -DestinationPath C:\ ;     Move-Item "C:/gnatsd-$($env:NATS_VERSION)-windows-amd64" 'c:/gnatsd';     Remove-Item gnatsd.zip
# Wed, 12 Jul 2017 18:22:29 GMT
WORKDIR C:\gnatsd
# Wed, 12 Jul 2017 18:22:32 GMT
COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Wed, 12 Jul 2017 18:22:34 GMT
EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Wed, 12 Jul 2017 18:22:36 GMT
ENTRYPOINT ["gnatsd"]
# Wed, 12 Jul 2017 18:22:38 GMT
CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6a43ac69611f40511708beba10dfe6fbe3e266ca933b6fd49c87a9f31f46f46c`  
		Size: 116.0 MB (116037241 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:acc75acac61e9635ae7c57f4d74b6ac6a2efef41d7b17052ff6f5bc0fb92e960`  
		Last Modified: Wed, 26 Apr 2017 19:51:40 GMT  
		Size: 968.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b292fea1ffba62db5e3476a2006b1c954c2152d66860b6b4da1ab4c4a6ce713f`  
		Last Modified: Wed, 12 Jul 2017 18:23:31 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1d76d0e36c57cffa79534f27f416f6e6df78bd5e91611f14db49a67422bfa6`  
		Last Modified: Wed, 12 Jul 2017 18:23:31 GMT  
		Size: 3.0 MB (3017643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed743a36ffb6c576310af25a32fe705badd1de465bfea12d62b9df07e4a47295`  
		Last Modified: Wed, 12 Jul 2017 18:23:29 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c79b4150aa9cfe22f5b3daf01c53b5dbf19e07f0d483152bf762f344f84b9a8`  
		Last Modified: Wed, 12 Jul 2017 18:23:28 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacdc36a9584bd1f4c8dab2f7ce691179494768ffd022ccc161248b1567707ad`  
		Last Modified: Wed, 12 Jul 2017 18:23:28 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d6f70defe410bac231f72d225bec05803336cd1aefd2f394e66afe57360c3d`  
		Last Modified: Wed, 12 Jul 2017 18:23:28 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5630869082075ca57a50085e6071a7461076364c329963176f3015355e378fa`  
		Last Modified: Wed, 12 Jul 2017 18:23:28 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
