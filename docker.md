## Docker commands

#### Regualar commands

`docker ps` : List all containers <br/>
`   -a`: stopped containers <br/>
`docker run -it <name> <image> bash|sh`: starts container and executes __bash__ or __sh__

__Entrypoint__: `docker run -it --entrypoint "bash" <image>`: starts container and executes __bash__ or __sh__
