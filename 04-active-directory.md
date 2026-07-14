# Active Directory Domain Services

## Objetivo

Transformar o Windows Server em um Controlador de Domínio (Domain Controller).

---

## Instalação da Função

Foi instalada a Role:

Active Directory Domain Services (AD DS)

Durante a instalação também foi instalado automaticamente:

- DNS Server

---

## Promoção do Servidor

Após a instalação da Role, o servidor foi promovido para Domain Controller.

Foi criada uma nova Forest.

Domínio

klatec.local

NetBIOS

KLATEC

O servidor passou a responder como Controlador de Domínio do ambiente.

---

## O que aconteceu durante a promoção

Durante a promoção foram executadas diversas configurações automaticamente pelo Windows Server.

Entre elas:

- criação da Forest
- criação do Domain
- instalação do DNS
- criação do banco NTDS.dit
- configuração do serviço Kerberos
- criação do Global Catalog
- preparação da estrutura inicial do Active Directory

---

## Estrutura criada automaticamente

KLATEC.LOCAL

- Builtin
- Computers
- Domain Controllers
- Users
- ForeignSecurityPrincipals

---

## Ferramentas disponíveis após a instalação

- Active Directory Users and Computers
- DNS Manager
- Active Directory Sites and Services
- Active Directory Domains and Trusts

---

## Capturas

- Assistente de instalação
- Promote this server to a domain controller
- Active Directory Users and Computers
- DNS Manager
- Server Manager