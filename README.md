# Projeto 01 - DevOps com Vagrant e Ansible

## 📌 Sobre o Projeto
[cite_start]Este repositório contém a infraestrutura como código (IaC) desenvolvida para o **Projeto 01** da disciplina de **Administração de Sistemas Abertos** (2025.2), ministrada pelo Prof. Leonidas Lima no **IFPB - Campus João Pessoa**[cite: 3, 7, 8, 9].

[cite_start]O objetivo principal é provisionar um ambiente virtual automatizado e configurar serviços essenciais utilizando **Vagrant** e **Ansible**[cite: 18, 19].

## 🏗️ Arquitetura do Ambiente
[cite_start]O projeto consiste em 4 máquinas virtuais (VMs) baseadas em **Debian 12 (Bookworm)** utilizando o provider **VirtualBox**[cite: 22, 24, 25].

As máquinas são:
* [cite_start]**arq (Servidor de Arquivos):** Responsável por DHCP, DNS, LVM e compartilhamento NFS[cite: 32, 85, 96, 104].
* [cite_start]**db (Banco de Dados):** Servidor rodando MariaDB[cite: 36, 124].
* [cite_start]**app (Aplicação):** Servidor Web Apache[cite: 50, 127].
* [cite_start]**cli (Cliente):** Estação de trabalho com interface gráfica (Firefox e X11)[cite: 53, 131].

## 🛠️ Tecnologias Utilizadas
* Vagrant
* VirtualBox
* Ansible
* Linux (Debian)
* Shell Script

## 📋 Pré-requisitos
Para executar este projeto, certifique-se de ter instalado:
* VirtualBox
* Vagrant
* Ansible

## 🚀 Como Executar
1. Clone este repositório:
   ```bash
   git clone <url-do-seu-repositorio>
   cd <nome-do-repositorio>

2.  Inicialize o ambiente com o Vagrant:

    ```bash
    vagrant up
    ```

3.  O provisionamento e configuração das máquinas serão gerenciados pelos Playbooks do Ansible.

## 👤 Autor

  * **Victor Henrique Santos Ferreira**

-----

*Projeto desenvolvido para fins educacionais no Instituto Federal da Paraíba.*
