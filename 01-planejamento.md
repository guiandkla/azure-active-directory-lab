# Planejamento da Infraestrutura

## Objetivo

Construir um laboratório corporativo utilizando Microsoft Azure e Windows Server para estudo de Active Directory Domain Services (AD DS), DNS, Group Policy (GPO), PowerShell e administração de ambientes Microsoft.

O laboratório foi desenvolvido seguindo boas práticas de infraestrutura utilizadas em empresas, permitindo simular um ambiente corporativo completo.

---

## Tecnologias Utilizadas

- Microsoft Azure
- Windows Server 2022 Datacenter Azure Edition
- Active Directory Domain Services (AD DS)
- DNS Server
- PowerShell
- Remote Desktop Protocol (RDP)

---

## Arquitetura Inicial

- 1.0 Azure Subscription
   - 1.1 Resource Group
   - 1.2 Virtual Network
   - 1.3 Domain Controller
   - 1.4 Cliente Windows 11

---

## Objetivos do Projeto

- Aprender Active Directory
- Aprender DNS
- Aprender Group Policy
- Aprender PowerShell
- Aprender administração Windows Server
- Documentar toda a implantação
- Criar um projeto de portfólio

---

## Decisões Técnicas

1) Por que criar um Resource Group?

Um Resource Group (RG) é um contêiner lógico utilizado para organizar e gerenciar recursos relacionados no Azure. Ele facilita a administração do ambiente, permitindo aplicar permissões (RBAC), políticas, monitoramento e controle de custos sobre um conjunto de recursos. Em ambientes corporativos, é comum criar RGs separados por projeto, ambiente (desenvolvimento, homologação e produção) ou departamento. Diferentemente do Active Directory, ele não organiza usuários, mas sim os recursos da infraestrutura em nuvem.

2) Por que utilizar uma Virtual Network?

A Virtual Network (VNet) fornece uma rede privada no Azure, permitindo que máquinas virtuais e outros recursos se comuniquem de forma segura, semelhante a uma rede local corporativa. Ela possibilita segmentação por sub-redes, controle de tráfego por meio de Network Security Groups (NSGs) e integração com redes locais via VPN ou ExpressRoute. Dessa forma, facilita a administração, a escalabilidade e a segurança da infraestrutura.

3) Por que um Domain Controller precisa de um IP privado estático?

O Domain Controller deve possuir um endereço IP privado estático para que clientes e servidores consigam localizá-lo de forma consistente. Como o Active Directory depende do serviço de DNS para autenticação e localização de recursos, uma mudança no endereço IP poderia impedir que computadores encontrassem o controlador de domínio. O uso de um IP fixo garante estabilidade, disponibilidade e o correto funcionamento dos serviços do AD DS.

4) O que é uma Forest?

Uma Forest (Floresta) é a estrutura lógica de mais alto nível do Active Directory. Ela reúne um ou mais domínios que compartilham um mesmo esquema, configuração e catálogo global, estabelecendo uma relação automática de confiança entre eles. Em laboratórios simples, normalmente existe apenas uma floresta contendo um único domínio.

5) O que acontece quando um servidor é promovido a Domain Controller?

Ao ser promovido a Domain Controller, o servidor passa a hospedar o banco de dados do Active Directory e assume a responsabilidade por autenticar usuários e computadores do domínio. Também instala e integra o serviço DNS, cria ou ingressa em uma floresta e domínio, além de armazenar objetos como usuários, grupos, computadores e políticas. Em ambientes com múltiplos DCs, a administração é compartilhada entre eles por meio da replicação.
