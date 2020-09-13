# Container
## Diferenças entre
![lxc-vm](images/lxc-vm.jpg)
* VM: Virtualização a nível de "Hardware"
* Container: Virtualização a nível de "Sistema Operacional"/Software
  * LXC - Linux Containers
  * Docker - <3
    * Trabalha com camadas (commits)
    * Apenas a ultima camada é RW
# Docker
* Instalação
```bash
curl -fsSL https://get.docker.com | bash
```
* Container 
  * Run
  ```bash
  docker container run  hello-world
  docker container run -ti debian bash
  docker container run -p 80:80 nginx 
  docker container run -d -p 80:80 --name meucontainer nginx 
  ```
  * Logs
  ```bash
  docker container logs meucontainer
  docker container logs -f meucontainer
  ```
  * Start/Stop
    * Iniciar e Parar um container já criado.
  * Ls/Inspect
    * Listar e Mostrar todos os detalhes dos containers.
  * Rm/Prune
    * Remover um container e Remover todos os containers que não estão sendo executados.
* Volume
  * Tipos
    * Volume - Volume "gerenciado" pelo docker
    * Bind - Diretório do S.O. "montado" no docker
  * Create
  ```bash
  docker volume create meuvolume
  ```
  * Ls/Inspect
    * Listar e Mostrar todos os detalhes dos volumes.
  * Rm/Prune
    * Remover uma rede e Remover todos os volume que não estão 'attachados' em algum container.
* Network
  * Create
  ```bash
  docker network create minharede
  ```
  * Ls/Inspect
    * Listar e Mostrar todos os detalhes das redes.
  * Rm/Prune
    * Remover uma rede e Remover todos as redes que não estão 'attachados' em algum container.
* DockerFile/Docker Hub
* Swarm
  * Criando cluster (Nó master)
  ```bash
  docker swarm init
  ```
  * Adicionando nós
  ```bash
   docker swarm join --token <TOKEN> <IPMASTER>:2377
  ```
  * Verificando nós
  ```bash
  docker node ls
  ```
  * Provendo nós de worker para master
  ```bash
  docker node promote <NOMEDONÓ>
  ```
  * Service
    * Create
      * Cria um serviço
    * Ls/Ps/Inspect 
      * Listar os serviço, detalhes de um serviço
    * Logs
      * Mostrar logs de um serviço
    * Scale
      * Escalar um serviço
  * stack

# Referencias
* [Docker Documentation](https://docs.docker.com/)
* [Livro: Docker Para Desenvolvedores](https://leanpub.com/dockerparadesenvolvedores)
* [Livro: Descomplicando o Docker](https://www.amazon.com.br/dp/B01M4P01VI)
* [Canal Youtube LinuxTips](https://www.youtube.com/linuxtips)
* [Mundo Docker](https://www.mundodocker.com.br)