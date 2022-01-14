# Docker

Open Docker Logs
```
make logs
```
Run Webpack Once
```
make webpack
```
Run Webpack & Watch
```
make webpackwatch
```
Run Typescript Build
```
make tsc
```
Open Container Bash
```
make bash
```
Run Command in Container
```
docker exec -it katanio <command>
```
Stop Image
```
make stop
```

Build Scss
```
make css
```

## Build
Build For Development & watch docker logs (Local)
```
make dev
```
Build For Staging (Bitmaze)
```
make staging
```
Build For Production (Katan)
```
make production
```

## Clean
Clean Katanio Image (If node modules, docker, environment changes)
```
make clean
```
Clean All Images
```
make clean-all
```
Clean files not in git repo
```
make cleangit
```

## Stats
Show active containers
```
docker ps -a
```
Container resource usage
```
docker stats
```

## Extra
Pause container
```
docker pause katanio
```
Unpause container
```
docker unpause katanio
```
Stop container
```
docker stop katanio
```
Connect to other container bash
```
docker exec -it katanio bash
``` 
Show environment variables
```
docker exec -it katan printenv
```
Remove Container
```
docker rm katanio
```
Remove Image
```
docker rmi katanio
```
Delete Folder
```
rm -rf katan
```
Delete Everything
```
docker system prune -a
```
Delete All Containers
```
docker rm -f $(docker ps -a -q)
```

## Info

- The system is designed to work only in using docker.
- If node_modules changes in any way, a new container must be built `make development-build` or `make clean` and `make dev`
- Every other change can be done either editing files in docker or files in host.

