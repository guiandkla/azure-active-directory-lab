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
<img width="1908" height="787" alt="Screenshot 2026-07-13 174144" src="https://github.com/user-attachments/assets/10a0bd43-52f6-4b8e-9d58-befdc5dfb9bc" />

- Máquina Virtual
<img width="1907" height="919" alt="Screenshot 2026-07-13 173909" src="https://github.com/user-attachments/assets/adbb42fa-489b-438c-b3f8-949edbf08f2e" />

- Virtual Network
<img width="1896" height="924" alt="Screenshot 2026-07-13 174534" src="https://github.com/user-attachments/assets/2d77ff56-aa30-4edb-ac39-30dfc96ac16d" />
