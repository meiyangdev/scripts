```
docker exec -it constainer-id /bin/bash 
bundle exec rails console
```
check dead docker container logs:
```
docker ps -a
docker logs --tail 100 --follow dead container_id 0334f8adad3d
If the container is dead or exited, --follow may not show anything (since the container isn’t running).

docker logs --tail 100 container_id
```
start local devcontainer
`devcontainer exec --workspace-folder . /bin/bash`