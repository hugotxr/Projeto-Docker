# Projeto de Administração de Sistemas Abertos - IFPB

Este projeto automatiza a criação de um ambiente **WordPress** completo utilizando Vagrant , ansible e Docker 

## 📋 Sobre o Projeto
O objetivo é provisionar uma infraestrutura completa via código (IaC), onde:
1.  **Vagrant** cria a máquina virtual (Debian Bookworm).
2.  **Ansible** configura o ambiente e instala o Docker.
3.  **Docker Compose** orquestra 3 containers:
    * **WebProxy:** Nginx personalizado (Load Balancer Camada 4).
    * **WebServer:** WordPress oficial.
    * **Database:** MySQL oficial.

## 🚀 Tecnologias Utilizadas
* Vagrant
* Ansible
* Docker & Docker Compose
* VirtualBox
* Nginx (Imagem personalizada: `hugotxr/nginx-custom`)

## 🛠️ Pré-requisitos
* VirtualBox instalado.
* Vagrant instalado.
* Git instalado.

## ▶️ Como Executar
1-Clone esse repositorio
2-Vagrant up
3-acesse no navegador http://192.168.56.154:8080
4-vagrant ssh
5-sudo docker exec -it webproxy curl -I localhost:8080
