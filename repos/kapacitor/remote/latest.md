## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:3ac4585ff8d338887ec4bb71e17e6f816b509a62740ec3e733fe2fdcef120a0f
```

-	Platforms:
	-	linux; amd64

### `kapacitor:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102625702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fb75e206b1796eb5128fe1d1546d8ab131e09d7ec0eca73f704ad7eae87e8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 20 Jun 2017 20:13:32 GMT
ADD file:9c48682ff75c756544d4491472081a078edf5dd0bb5038d1cb850a1f9c480e3e in / 
# Tue, 20 Jun 2017 20:13:34 GMT
CMD ["bash"]
# Tue, 20 Jun 2017 21:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Jul 2017 22:11:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 14 Jul 2017 21:26:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 14 Jul 2017 21:26:23 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 14 Jul 2017 21:26:24 GMT
ENV KAPACITOR_VERSION=1.3.1
# Fri, 14 Jul 2017 21:26:29 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Fri, 14 Jul 2017 21:26:30 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Fri, 14 Jul 2017 21:26:31 GMT
EXPOSE 9092/tcp
# Fri, 14 Jul 2017 21:26:31 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Jul 2017 21:26:32 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Fri, 14 Jul 2017 21:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Jul 2017 21:26:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9f0706ba7422412cd468804fee456786f88bed94bf9aea6dde2a47f770d19d27`  
		Last Modified: Tue, 20 Jun 2017 20:35:47 GMT  
		Size: 52.6 MB (52614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3942a742d221ef22a0a335c4eebf09e15a36dcfb224b5a2d0cdcc405f374ccb`  
		Last Modified: Wed, 21 Jun 2017 00:33:28 GMT  
		Size: 19.3 MB (19264368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7b031c44274e2e00173b5912a1e74ca92c420278d39af4347ae0632301faef`  
		Last Modified: Fri, 14 Jul 2017 21:27:32 GMT  
		Size: 10.0 MB (10000321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c54fc245846c0599aa3d4d4c82dd0bdf104064e859c0c1612c765e9c2b0985`  
		Last Modified: Fri, 14 Jul 2017 21:27:30 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97faa6fec8bf4c740033a9b5609f0ec3954b4251578dd9e757c1e7d7113750fc`  
		Last Modified: Fri, 14 Jul 2017 21:27:35 GMT  
		Size: 20.7 MB (20738959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ef0b8419787e87143164a7511eccd0c333ec5801a9f5c7f536186c10e54fe`  
		Last Modified: Fri, 14 Jul 2017 21:27:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c5c4b3dfed7d42d94a36c60310cc79062652b75c886b8850f014cfa964c1b1`  
		Last Modified: Fri, 14 Jul 2017 21:27:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
