## `swarm:latest`

```console
$ docker pull swarm@sha256:1a05498cfafa8ec767b0d87d11d3b4aeab54e9c99449fead2b3df82d2744d345
```

-	Platforms:
	-	linux; amd64

### `swarm:latest` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecf8baf8eae79fe300b4c7f55e490e508ccb67ffa54b1b99162850616c68fcb`
-	Entrypoint: `["\/swarm"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 11 Jul 2017 19:09:01 GMT
COPY file:68bb308564ed8a5ab3947f9312203ba536151a2f0bb9f62af59ef9c6f657cae3 in /swarm 
# Tue, 11 Jul 2017 19:09:21 GMT
COPY file:7544fce8b63059c6e70ecf475487d6e4ea6fef407369869f02d8ea84b211c4de in /etc/ssl/certs/ca-certificates.crt 
# Tue, 11 Jul 2017 19:09:35 GMT
COPY dir:d556676b4fb31ddaa271490e57c3a85e3c4bcc1e809b22d64b2f570c05149a22 in /tmp 
# Tue, 11 Jul 2017 19:09:49 GMT
ENV SWARM_HOST=:2375
# Tue, 11 Jul 2017 19:09:56 GMT
EXPOSE 2375/tcp
# Tue, 11 Jul 2017 19:10:10 GMT
VOLUME [/.swarm]
# Tue, 11 Jul 2017 19:10:24 GMT
ENTRYPOINT ["/swarm"]
# Tue, 11 Jul 2017 19:10:37 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:ad8c679cee1a0d21675737fe3eae76c6ed5dee1f1c01e20c6645daca39d88ebc`  
		Last Modified: Tue, 11 Jul 2017 19:11:15 GMT  
		Size: 4.4 MB (4426357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97186f5f56a98d05de40232904087e7e7b4b3ae78f6579dd17e381d17f0f3ad3`  
		Last Modified: Tue, 11 Jul 2017 19:11:15 GMT  
		Size: 156.8 KB (156761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821a304aaa0dbe477c47d14eb0e38a234594111cb399763450efe30c90893522`  
		Last Modified: Tue, 11 Jul 2017 19:11:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
