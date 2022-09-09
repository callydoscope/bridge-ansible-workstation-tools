# Workstation Tools

Este repositório possui scripts para automatizar e agilizar o 'workflow' e a preparação do ambiente pós-instalação.

> A execução deste script somente é executado em ambientes Gnome-Like. Ou seja, qualquer distribuição Linux que possua comandos como: Sudo, Apt, Apt-get, etc.

## Sobre Ansible

Ansible é uma ferramenta de automação para provisionamento, gerenciamento de configurações e orquestração de ambientes.

Por padrão, ele utiliza a linguagem YAML para escrever o Ansible Playbook. Este, por sua vez, permite você escrever suas tarefas automatizadas.

## Preparando o ambiente

> Para fins de dúvida analise o arquivo `main.yml` antes de realizar a instalação para ter certeza que deseja instalar todas as aplicações que estão inseridas nele.

1. Instalar Ansible na máquina

```bash
sudo apt update && sudo apt install ansible unzip git -y
```

2. Clonar esse repositório

```bash
git clone https://github.com/callydoscope/bridge-ansible-workstation-tools.git && cd bridge-ansible-workstation-tools
```

## Executando

1. Instalar aplicações no Ansible-Playbook

```bash
ansible-playbook roles/common/tasks/main.yml --ask-become-pass
```

> Após inserir o comando acima no Terminal, lembre-se de digitar sua senha root da máquina.
___
