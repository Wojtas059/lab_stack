### Sprawozdanie 
> Wojciech Maj, 2.2/4

link do mojego profilu na DOckerHub
https://hub.docker.com/repository/docker/wojmaj/lab_4

Polecenia:
```cmd
docker buildx create --name testbuilder
```
```cmd
docker buildx use testbuilder
```
```cmd
docker buildx inspect --bootstrap
```
```cmd
docker buildx build -t wojmaj/lab_4:tagname --platform linux/amd64,linux/arm64,linux/arm/v7,linux/arm/v6 --push .
```
```cmd

docker buildx imagetools inspect wojmaj/lab_4:tagname
Name:      docker.io/wojmaj/lab_4:tagname
MediaType: application/vnd.docker.distribution.manifest.list.v2+json
Digest:    sha256:7d036563d6bd810cc5c3939c42d453052221f8627687352a508ce03fd2ea31f3
           
Manifests: 
  Name:      docker.io/wojmaj/lab_4:tagname@sha256:32d7e84a059942f329903bd34aca13c9a1e8598b6a2541c211154b7900e8bb17
  MediaType: application/vnd.docker.distribution.manifest.v2+json
  Platform:  linux/amd64
             
  Name:      docker.io/wojmaj/lab_4:tagname@sha256:3801dcbd5ad7b43648d73e5e201bcc9074cdbee6fb068008879f3fe2233b086f
  MediaType: application/vnd.docker.distribution.manifest.v2+json
  Platform:  linux/arm64
             
  Name:      docker.io/wojmaj/lab_4:tagname@sha256:4c973aba07db20f021ce9e7e600515673c4ef609eebbfcc7bcb4266d8052c30c
  MediaType: application/vnd.docker.distribution.manifest.v2+json
  Platform:  linux/arm/v7
             
  Name:      docker.io/wojmaj/lab_4:tagname@sha256:ecb0f75ca45abfb65399c39a9609e406685894053388aef1dc9eedbf3d216026
  MediaType: application/vnd.docker.distribution.manifest.v2+json
  Platform:  linux/arm/v6

```

