# AWS – Principais Serviços (Resumo para estudo)

Este material apresenta os principais serviços da AWS com explicações mais profundas, ideal para estudo estruturado e revisão para certificações.

---

<details>
<summary><strong>IAM (Identity and Access Management)</strong></summary>

### O que é
O IAM é o serviço responsável por gerenciar **identidades e permissões** dentro da conta AWS. Ele controla autenticação (quem pode acessar) e autorização (o que pode fazer).

### Componentes principais
- **Usuários:** Identidades individuais para pessoas ou sistemas.
- **Grupos:** Conjunto de usuários com permissões semelhantes.
- **Policies:** Documentos JSON que definem ações permitidas ou negadas.
- **Roles (Funções):** Permissões temporárias assumidas por serviços ou aplicações.
- **MFA (Multi-Factor Authentication):** Camada adicional de segurança.

### Conceitos fundamentais
- **Princípio do menor privilégio:** Conceder apenas as permissões necessárias.
- **Credenciais temporárias:** Mais seguras do que credenciais fixas.
- **Root user:** Deve ser usado apenas para tarefas administrativas críticas.

### Por que é essencial
- Base da segurança na AWS
- Permite auditoria via CloudTrail
- Reduz riscos de acesso indevido

### Cenários práticos
- Criar usuários para equipe de desenvolvimento
- Permitir que uma aplicação EC2 acesse o S3 usando Role
- Restringir acesso a produção

</details>

---

<details>
<summary><strong>VPC (Virtual Private Cloud)</strong></summary>

### O que é
A VPC é uma rede virtual isolada dentro da AWS onde você define IPs, sub-redes, rotas e regras de segurança.

### Componentes principais
- **CIDR Block:** Faixa de IP da rede (ex: 10.0.0.0/16).
- **Subnets:** Divisão da rede (pública ou privada).
- **Route Tables:** Definem para onde o tráfego será direcionado.
- **Internet Gateway:** Permite acesso à internet.
- **NAT Gateway:** Permite saída para internet em subnets privadas.
- **Security Groups e NACLs:** Camadas de firewall.

### Conceitos fundamentais
- Subnets públicas possuem rota para Internet Gateway.
- Subnets privadas não possuem acesso direto à internet.
- Separação de camadas (web, app, db) aumenta segurança.

### Por que é essencial
- Base de qualquer arquitetura segura
- Permite isolamento de ambientes (dev, homolog, prod)
- Controla comunicação entre recursos

### Cenários práticos
- Criar arquitetura com servidor web público e banco privado
- Configurar NAT para atualizações em instâncias privadas

</details>

---

<details>
<summary><strong>EC2 (Elastic Compute Cloud)</strong></summary>

### O que é
Serviço de máquinas virtuais sob demanda, permitindo controle total do sistema operacional.

### Componentes principais
- **Instâncias:** Servidores virtuais.
- **AMI:** Imagem base para criação da instância.
- **Tipos de instância:** Otimizados para CPU, memória ou armazenamento.
- **EBS:** Armazenamento em bloco persistente.
- **Elastic IP:** IP público fixo.

### Conceitos fundamentais
- Escalabilidade vertical (trocar tipo de instância)
- Escalabilidade horizontal (múltiplas instâncias)
- Monitoramento via CloudWatch

### Por que é essencial
- Flexibilidade total de configuração
- Ideal para aplicações legadas ou customizadas
- Base para ambientes tradicionais

### Cenários práticos
- Hospedar API em PHP
- Criar servidor para testes
- Executar aplicação corporativa

</details>

---

<details>
<summary><strong>S3 (Simple Storage Service)</strong></summary>

### O que é
Serviço de armazenamento de objetos altamente escalável e durável.

### Componentes principais
- **Buckets:** Containers lógicos.
- **Objetos:** Arquivos armazenados.
- **Versionamento:** Histórico de versões.
- **Lifecycle Rules:** Automação de transição ou exclusão.
- **Storage Classes:** Standard, IA, Glacier.

### Conceitos fundamentais
- Durabilidade de 99.999999999%
- Armazenamento ilimitado
- Pode hospedar sites estáticos

### Por que é essencial
- Backup confiável
- Armazenamento econômico
- Base para Data Lakes

### Cenários práticos
- Armazenar uploads de usuários
- Backup de banco de dados
- Guardar logs de aplicação

</details>

---

<details>
<summary><strong>RDS (Relational Database Service)</strong></summary>

### O que é
Serviço gerenciado de banco de dados relacional, onde a AWS cuida da infraestrutura.

### Engines suportadas
MySQL, PostgreSQL, MariaDB, Oracle, SQL Server e Aurora.

### Componentes principais
- **Instância de banco**
- **Multi-AZ:** Alta disponibilidade automática.
- **Read Replicas:** Escalabilidade de leitura.
- **Snapshots:** Backup manual.
- **Parameter Groups:** Configuração do banco.

### Conceitos fundamentais
- Backup automático configurável
- Failover automático em Multi-AZ
- Escalabilidade vertical simples

### Por que é essencial
- Reduz trabalho operacional
- Alta disponibilidade integrada
- Segurança gerenciada

### Cenários práticos
- Sistema web com banco relacional
- API com persistência de dados
- Aplicação corporativa transacional

</details>

---

<details>
<summary><strong>ECS (Elastic Container Service)</strong></summary>

### O que é
Serviço de orquestração de containers Docker.

### Componentes principais
- **Cluster:** Infraestrutura onde containers rodam.
- **Task Definition:** Configuração do container.
- **Task:** Execução da definição.
- **Service:** Mantém número fixo de containers ativos.
- **Fargate:** Execução sem gerenciar servidores.

### Conceitos fundamentais
- Escalabilidade automática
- Integração com Load Balancer
- Ideal para microsserviços

### Por que é essencial
- Facilita deploy de aplicações modernas
- Reduz complexidade de infraestrutura
- Integra com CI/CD

### Cenários práticos
- Deploy de API containerizada
- Microsserviços escaláveis
- Aplicações cloud-native

</details>

---

# Visão Estratégica Final

Esses serviços formam o núcleo da arquitetura AWS:

- IAM → Segurança
- VPC → Rede
- EC2 → Computação
- S3 → Armazenamento
- RDS → Banco de dados
- ECS → Containers

Dominar esses serviços é fundamental para arquiteturas seguras, escaláveis e modernas na AWS.
