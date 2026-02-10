# AWS (Resumo para Estudo)

A Amazon Web Services (AWS) é a principal plataforma de computação em nuvem do mercado, oferecendo uma ampla variedade de serviços para criar, hospedar e escalar aplicações de forma segura, flexível e sob demanda.

A AWS permite que empresas e desenvolvedores utilizem recursos computacionais via internet, pagando apenas pelo que for utilizado. Isso acelera o desenvolvimento, reduz custos e aumenta a confiabilidade dos sistemas.

Serão abordados serviços fundamentais como:

- **IAM** (Identity and Access Management)
   - Controle de usuários, permissões e segurança da conta AWS.

- **VPC** (Virtual Private Cloud)
   - Criação e gerenciamento de redes virtuais privadas na nuvem.

- **EC2** (Elastic Compute Cloud)
   - Provisionamento de servidores virtuais sob demanda.

- **S3** (Simple Storage Service)
   - Armazenamento de objetos com alta durabilidade e escalabilidade.

- **RDS** (Relational Database Service)
   - Banco de dados relacional gerenciado pela AWS.

- **ECS** (Elastic Container Service)
   - Execução e gerenciamento de aplicações em containers.

##  Seção 1: Identity and Access Management (IAM)

O **IAM** é o serviço da AWS responsável por **controle de acesso**, **autenticação** e **autorização**. Ele define **quem pode acessar** e **o que pode fazer** dentro da conta AWS.

---

### Adicionando MFA para Usuário Root

**O que é:**  
Ativação de **MFA (Multi-Factor Authentication)** para o usuário **Root** da conta AWS.

**Para que serve:**  
- Adiciona uma camada extra de segurança além da senha  
- Exige um código temporário (app ou token físico)  
- Protege a conta contra acessos indevidos  

**Boas práticas:**  
- O usuário Root **não deve ser usado no dia a dia**  
- Sempre habilitar MFA para o Root  

---

### Criando um Usuário Administrador

**O que é:**  
Criação de um usuário IAM com **permissões administrativas**.

**Para que serve:**  
- Evita o uso do usuário Root  
- Permite gerenciar recursos da AWS com segurança  
- Facilita auditoria e rastreabilidade de ações  

**Boas práticas:**  
- Conceder a política `AdministratorAccess`  
- Usar MFA também para esse usuário  

---

### Criando um Grupo de Usuário

**O que é:**  
Um **Grupo IAM** é um conjunto de usuários que compartilham as mesmas permissões.

**Para que serve:**  
- Facilita o gerenciamento de acessos  
- Evita configurar permissões usuário por usuário  
- Padroniza permissões por função  

---

### Gerenciando Política de Senha

**O que é:**  
Configuração das regras de senha para usuários IAM.

**Para que serve:**  
- Força senhas mais seguras  
- Reduz riscos de ataques por força bruta  

---

### Criando Política de Usuário

**O que é:**  
Política IAM define **quais ações são permitidas ou negadas**.

**Para que serve:**  
- Controlar acesso a serviços e recursos  
- Aplicar o princípio do **menor privilégio**  

---

## Seção 2: Virtual Private Cloud (VPC)

A **VPC** permite criar uma **rede virtual isolada** dentro da AWS.

---

### Introdução à VPC

**O que é:**  
Uma **rede virtual privada** na AWS, totalmente configurável.

**Para que serve:**  
- Isolamento de rede  
- Controle de tráfego  

---

### Criando a VPC

**O que é:**  
Criação da rede principal com um **CIDR Block**.

**Para que serve:**  
- Define o espaço de IPs da rede  

---

### Criando a Sub-rede (Subnet)

**O que é:**  
Divisão da VPC em redes menores.

**Para que serve:**  
- Organizar recursos  
- Separar ambientes públicos e privados  

---

### Route Table

**O que é:**  
Tabela que define **para onde o tráfego de rede vai**.

**Para que serve:**  
- Controlar rotas internas e externas  

---
