# Biblioteca Municipal Ney Pontes — F5.3.6

Projeto Ruby on Rails do desafio de seleção de estagiários da Prefeitura de Mossoró/RN.

## O que já está incluído
- Autenticação de bibliotecário por sessão.
- Cadastro/login de bibliotecários.
- Categorias.
- CRUD de livros.
- CRUD de usuários.
- Empréstimos conectando usuário + livro.
- Devolução e histórico.
- Bloqueio de exclusão de usuário com histórico.
- Dashboard com contadores.
- Estrutura para envio de senha de empréstimo por e-mail.
- Comentários explicando a função das principais partes do código.

## Segurança
Nunca coloque senha de Gmail ou qualquer segredo diretamente no código. Configure SMTP por variáveis de ambiente.

Exemplo:
SMTP_ADDRESS=smtp.gmail.com
SMTP_PORT=587
SMTP_USERNAME=seu-email@gmail.com
SMTP_PASSWORD=sua-senha-de-app

## Instalação
```bash
bundle install
bin/rails db:create db:migrate
bin/rails server
```

Acesse http://localhost:3000

## Observação
Este pacote reúne a implementação consolidada das etapas produzidas até F5.3.6. Antes de entregar, execute os testes e revise as regras específicas do edital.
