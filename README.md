# vngn
# Biblioteca Municipal Ney Pontes

Sistema web para gerenciamento do acervo, usuários e empréstimos da **Biblioteca Municipal Ney Pontes**, localizada em Mossoró/RN.

Projeto desenvolvido para o **Desafio nº 0001/2026 — Seleção de Estagiários para a Prefeitura de Mossoró**.

## 📚 Sobre o projeto

O sistema tem como objetivo digitalizar o gerenciamento da biblioteca, substituindo controles manuais por uma aplicação moderna, segura, responsiva e organizada.

A plataforma permite cadastrar livros, categorias e usuários, controlar empréstimos e devoluções, acompanhar atrasos e consultar históricos.

## ⚙️ Principais funcionalidades

* 🔐 Login e autenticação de bibliotecários
* 🔑 Recuperação e alteração de senha
* 👨‍💼 Cadastro de bibliotecários
* 📚 Cadastro e gerenciamento de livros
* 🏷️ Cadastro de categorias
* 👤 Cadastro e gerenciamento de usuários
* 🔎 Pesquisa e filtros
* 📖 Registro de empréstimos
* 🔄 Registro de devoluções
* 📅 Cálculo de 15 dias úteis para devolução
* 🔑 Confirmação de empréstimo por senha
* ⏰ Controle de empréstimos atrasados
* 🔄 Renovação de empréstimos
* 📜 Histórico de empréstimos
* 💰 Cálculo de multas
* 📊 Dashboard administrativo
* 📈 Relatórios
* 📱 Interface responsiva
* 🛡️ Validações e recursos de segurança

## 🛠️ Tecnologias

* Ruby
* Ruby on Rails
* PostgreSQL
* HTML5
* CSS3
* JavaScript
* Bootstrap ou Tailwind CSS
* Stimulus / Hotwire

## 🏗️ Arquitetura

O projeto segue o padrão **MVC (Model-View-Controller)** do Ruby on Rails.

Principais entidades:

* Bibliotecários
* Categorias
* Livros
* Usuários
* Empréstimos
* Tokens de recuperação de senha

Os relacionamentos entre essas entidades permitem controlar todo o fluxo de empréstimo e devolução.

## 💾 Banco de dados

O sistema utiliza banco de dados real para armazenar as informações.

Principais relacionamentos:

* Uma categoria possui vários livros.
* Um livro pertence a uma categoria.
* Um livro possui vários empréstimos.
* Um usuário possui vários empréstimos.
* Um bibliotecário pode registrar vários empréstimos.
* Um empréstimo pertence a um livro, usuário e bibliotecário.

## 🚀 Instalação

### 1. Clonar o projeto

```bash
git clone <URL_DO_REPOSITORIO>
cd biblioteca_ney_pontes
```

### 2. Instalar as dependências

```bash
bundle install
```

### 3. Configurar o banco de dados

Configure o PostgreSQL e as variáveis necessárias no arquivo de ambiente.

Depois execute:

```bash
rails db:create
rails db:migrate
```

### 4. Criar dados de demonstração

```bash
rails db:seed
```

### 5. Iniciar o servidor

```bash
rails server
```

A aplicação estará disponível localmente no endereço configurado pelo Rails.

## 🔐 Variáveis de ambiente

Exemplo de informações que podem ser necessárias:

```env
DATABASE_URL=
SMTP_ADDRESS=
SMTP_PORT=
SMTP_USERNAME=
SMTP_PASSWORD=
```

**Importante:** não coloque senhas, tokens ou outras credenciais reais diretamente no código ou no GitHub.

## 👤 Usuário de demonstração

O projeto deve utilizar apenas credenciais fictícias para apresentação.

Exemplo:

```text
E-mail: admin@biblioteca.local
Senha: Admin@123
```

Altere essas credenciais conforme a configuração dos seeds do projeto.

## 📖 Fluxo principal

```text
Login
  ↓
Dashboard
  ↓
Pesquisar livro
  ↓
Verificar disponibilidade
  ↓
Selecionar usuário
  ↓
Confirmar senha de empréstimo
  ↓
Registrar empréstimo
  ↓
Calcular 15 dias úteis
  ↓
Registrar devolução
  ↓
Atualizar disponibilidade
  ↓
Salvar histórico
```

## 📅 Regra de empréstimo

O prazo padrão de devolução é de **15 dias úteis**.

Sábados e domingos não são contabilizados.

O sistema registra:

* Data do empréstimo;
* Data prevista para devolução;
* Data real da devolução;
* Status do empréstimo;
* Dias de atraso;
* Multa, quando aplicável.

## 🎯 Funcionalidades extras

Além das funcionalidades principais, o projeto pode incluir:

* Renovação de empréstimos;
* Histórico completo;
* Controle de atrasos;
* Cálculo de multas;
* Relatórios;
* Dashboard com indicadores;
* Busca global;
* Melhorias de acessibilidade.

## 🔒 Segurança

O sistema utiliza boas práticas, incluindo:

* Senhas protegidas por hash;
* Autenticação;
* Controle de sessão;
* Proteção contra CSRF;
* Validação no backend;
* Tokens seguros para recuperação de senha;
* Controle de acesso;
* Validação de dados;
* Proteção contra SQL Injection e XSS.

## 📱 Responsividade

A interface foi planejada para funcionar em:

* Computadores;
* Notebooks;
* Tablets;
* Celulares.

## 🎤 Apresentação

O sistema foi estruturado para permitir uma demonstração de aproximadamente **8 minutos**, apresentando:

1. Login;
2. Dashboard;
3. Categorias;
4. Livros;
5. Usuários;
6. Pesquisa;
7. Empréstimo;
8. Confirmação por senha;
9. Prazo de 15 dias úteis;
10. Devolução;
11. Histórico;
12. Atrasos;
13. Renovação;
14. Multas;
15. Relatórios.

## 📌 Status do projeto

**Em desenvolvimento.**

O objetivo é entregar um sistema funcional, organizado e preparado para apresentação e publicação em um repositório GitHub.

## 👨‍💻 Projeto

**Biblioteca Municipal Ney Pontes — Mossoró/RN**

**Desafio nº 0001/2026 — Seleção de Estagiários para a Prefeitura de Mossoró**

---

Desenvolvido com foco em organização, segurança, facilidade de uso e digitalização dos processos da biblioteca.
