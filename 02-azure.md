# Microsoft Azure

## Objetivo

Criar toda a infraestrutura necessária para hospedar um Domain Controller utilizando máquinas virtuais do Microsoft Azure.

---

## Recursos Criados

### Resource Group

Foi criado um Resource Group para organizar todos os recursos do laboratório.

Nome: rg-klatec-lab

O Resource Group permite administrar todos os recursos do projeto em um único local.

---

### Virtual Network

Foi criada uma Virtual Network (VNet), responsável pela comunicação entre os servidores da infraestrutura.

Rede

10.0.0.0/16

Subnet

10.0.0.0/24

Gateway

10.0.0.1

---

### Máquina Virtual

Foi criada uma máquina virtual denominada:

dc01

Sistema Operacional

Windows Server 2022 Datacenter Azure Edition

A VM será utilizada como primeiro Controlador de Domínio da infraestrutura.

---

## Capturas de Tela

- Resource Group
- Virtual Network
- Máquina Virtual
- Configuração de Rede