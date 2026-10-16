# Web Quality Lab

Projeto de portfólio voltado à prática de testes de software, com foco em testes funcionais manuais de uma aplicação web.

## Objetivo

Praticar atividades de QA, elaborar casos de teste, registrar resultados reais, identificar comportamentos inesperados e documentar defeitos de forma organizada.

## Aplicação testada

- **Nome:** QA Practice Website
- **URL:** https://qaengineerwaqas.com/qa-practice
- **Tipo de teste:** Testes funcionais manuais
- **Ferramentas:** Visual Studio Code, Markdown, Git e GitHub

## Escopo dos testes

Foram explorados os seguintes cenários:

- Login com campos preenchidos.
- Validação de campos obrigatórios no login.
- Login com e-mail em formato inválido.
- Formulário de contato com campos vazios.
- Formulário de contato com preenchimento parcial.
- Formulário de contato com todos os campos preenchidos.

## Defeitos identificados

- **BUG-001 — Login:** a aplicação exibe uma mensagem de sucesso mesmo com dados fictícios ou e-mail em formato inválido, sem redirecionar para uma área interna.
- **BUG-002 — Formulário de contato:** a aplicação exibe uma mensagem de envio mesmo com campos vazios ou parcialmente preenchidos.

Os comportamentos foram registrados com base nas observações dos testes. Não foi confirmado se houve autenticação real ou envio efetivo de dados.

## Estrutura do projeto
```text
web-quality-lab/
├── README.md
├── docs/
│   ├── plano-de-testes.md
│   ├── casos-de-teste.md
│   └── relatorio-de-defeitos.md
└── evidencias/
    ├── BUG-001-login-sucesso.png
    ├── BUG-002-formulario-sem-validacao.png
    ├── CT-001-Login-com-campos-preenchidos.png
    ├── CT-002-Login-com-email-vazio.png
    └── CT-004-Login-com-email-em-formato-invalido.png
```


## Documentação

- [Plano de Testes](docs/plano-de-testes.md)
- [Casos de Teste](docs/casos-de-teste.md)
- [Relatório de Defeitos](docs/relatorio-de-defeitos.md)
- [Evidências](evidencias/)

## Status do projeto

Concluído — 7 casos de teste executados e 2 comportamentos documentados para investigação.

