# Docker
## Do Run ao Cluster
Hands-on com um overview sobre docker, mostrando de forma simples os principais comandos e boas práticas de uso.

* Install
* Docker User
* Docker Admin
* Docker Cluster

## PreReq
### Para 100% de Aproveitamento:
* Conta grátis no [cloudflare](https://cloudflare.com/);
* Conta grátis no [dot.tk](https://dot.tk);
  * Registrar um domínio grátis
* Conta na [AWS](https://aws.amazon.com);
  * EC2
    * 3 VMs (AWS t2.micro - free tier):
      * cpu: 1cpu
      * ram: 1Gib
      * disk: 8gb
      * Pode ser em outro player como [AZURE](https://azure.microsoft.com/en-us/), [GCP](cloud.google.com), [Digital Ocean](https://digitalocean.com) ou [Vultr](https://vultr.com).
  * RDS
    * MariaDB - FreeTier
  * EFS
    * Sistema

### Para 50% de Aproveitamento
* 3 VMs (Debian ou Ubuntu):
  * cpu: 1cpu
  * ram: 1Gib
  * disk: 8gb
* 1 VM com MariaDB instalado e acesso liberado pras 3VMs
* 1 VM com NFS Instalado e acesso liberado pras 3VMS
* Acesso "root" para editar arquivo /etc/hosts

## Meta
* [Minibio](minibio.md)
* [Topicos](topics.md)
* [Contatos](contacts.md)