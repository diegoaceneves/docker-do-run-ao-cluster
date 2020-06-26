# Container
## Diferenças entre
![lxc-vm](https://www.mundodocker.com.br/wp-content/uploads/2015/06/lxc-vm.jpg)
* VM: Virtualização a nível de "Hardware"
* Container: Virtualização a nível de "Sistema Operacional"/Software
  * LXC - Linux Containers
  * Docker - <3
    * Trabalha com camadas (commits)
    * Apenas a ultima camada é RW
# Docker
* Container 
  * Run
  ```bash
  docker container run  hello-world
  docker container run -ti debian bash
  docker container run -p 80:80 nginx 
  docker container run -d -p 80:80 -name meucontainer nginx 
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
  * Create
  * Ls/Inspect
  * Rm/Prune
* Network
  * Create
  * Ls/Inspect
  * Rm/Prune
* DockerFile/Docker Hub
* Service
  * Create
  * Ls/Ps/Inspect
  * Logs
  * Scale
* Swarm
  * Stack
# Referencias
* [Livro: Docker Para Desenvolvedores](https://leanpub.com/dockerparadesenvolvedores)
* [Livro: Descomplicando o Docker](https://www.amazon.com.br/dp/B01M4P01VI)
* [Canal Youtube LinuxTips](https://www.youtube.com/linuxtips)
* [Mundo Docker](https://www.mundodocker.com.br)