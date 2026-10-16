# Casos de Teste — Web Quality Lab

## 1. Informações do projeto

**Projeto:** Web Quality Lab  
**Tipo de teste:** Testes funcionais manuais  
**Aplicação testada:** https://qaengineerwaqas.com/qa-practice  
**Status:** Em andamento

## 2. Módulo: Login

### CT-001 — Login com dados fictícios em formato válido

**Objetivo:** Verificar o comportamento do login ao informar credenciais fictícias em formato válido, observando a mensagem apresentada e se ocorre redirecionamento para uma área interna.

**Pré-condição:** Estar na tela de login.

**Dados de teste:**
- E-mail: `teste@example.com`
- Senha: `SenhaTeste123`

**Passos executados:**
1. Preencher os campos de e-mail e senha.
2. Clicar no botão de login.
3. Observar a resposta da aplicação.

**Resultado esperado:** Resultado esperado: Como a aplicação não disponibiliza credenciais oficiais de teste, não é possível confirmar a autenticação esperada. A mensagem de sucesso deve corresponder a uma autenticação efetivamente realizada.

**Resultado obtido:** A aplicação exibiu `Login successful!`.

**Status:** Executado — comportamento em investigação.

### CT-002 — Login com e-mail vazio

**Objetivo:** Verificar o comportamento do login quando o e-mail não é informado.

**Passos executados:**
1. Deixar o campo de e-mail vazio.
2. Preencher o campo de senha.
3. Clicar no botão de login.

**Resultado esperado:** A aplicação deve solicitar o preenchimento do e-mail, caso seja obrigatório.

**Resultado obtido:** A mensagem `Preencha todos os campos` foi exibida.

**Status:** Executado — validação observada.

### CT-003 — Login com senha vazia

**Objetivo:** Verificar o comportamento do login quando a senha não é informada.

**Passos executados:**
1. Preencher o campo de e-mail.
2. Deixar o campo de senha vazio.
3. Clicar no botão de login.

**Resultado esperado:** A aplicação deve solicitar o preenchimento da senha, caso seja obrigatória.

**Resultado obtido:** A mensagem `Preencha todos os campos` foi exibida.

**Status:** Executado — validação observada.

### CT-004 — Login com e-mail em formato inválido

**Objetivo:** Verificar a resposta da aplicação a um e-mail em formato inválido.

**Dados de teste:**
- E-mail: `teste@`
- Senha: `SenhaTeste123`

**Passos executados:**
1. Informar o e-mail inválido.
2. Preencher o campo de senha.
3. Clicar no botão de login.
4. Observar a resposta.

**Resultado esperado:** O sistema deve rejeitar o formato inválido e não informar que o login foi bem-sucedido.

**Resultado obtido:** A mensagem `Login successful!` foi exibida. Não houve redirecionamento nem abertura de área interna.

**Status:** Executado — comportamento suspeito em investigação.


## 3. Módulo: Formulário de contato

### CT-005 — Envio do formulário com todos os campos vazios

**Objetivo:** Verificar se a aplicação valida o formulário quando nenhum campo é preenchido.

**Passos executados:**
1. Deixar todos os campos vazios.
2. Clicar no botão de envio.
3. Observar a mensagem exibida.

**Resultado esperado:** Se os campos forem obrigatórios, o formulário deve impedir o envio e informar quais campos precisam ser preenchidos.

**Resultado obtido:** Foi exibida a mensagem `Submitted! (Bug: no validation)`.

**Status:** Executado — validação em investigação.

### CT-006 — Envio do formulário com preenchimento parcial

**Objetivo:** Verificar se a aplicação valida os campos não preenchidos.

**Passos executados:**
1. Preencher somente os campos de nome e mensagem.
2. Deixar os demais campos vazios.
3. Clicar no botão de envio.
4. Observar a mensagem exibida.

**Resultado esperado:** Se os campos restantes forem obrigatórios, o formulário deve solicitar seu preenchimento.

**Resultado obtido:** Foi exibida a mensagem `Submitted! (Bug: no validation)`.

**Status:** Executado — validação em investigação.

### CT-007 — Envio do formulário com todos os campos preenchidos

**Objetivo:** Observar a resposta do formulário quando todos os campos estão preenchidos com dados fictícios em formato válido.

**Passos executados:**
1. Preencher todos os campos com dados fictícios válidos.
2. Clicar no botão de envio.
3. Observar a mensagem exibida.

**Resultado esperado:** A aplicação deve processar os dados válidos e apresentar uma confirmação apropriada, caso o envio seja concluído.

**Resultado obtido:** Foi exibida a mensagem `Submitted! (Bug: no validation)`.

**Status:** Executado — comportamento observado.

## 4. Observações gerais

- Os testes foram executados manualmente.
- O site não disponibiliza credenciais oficiais de teste.
- Os dados utilizados foram fictícios.
- As mensagens exibidas foram registradas conforme observadas durante a execução.
- A exibição de uma mensagem de sucesso não comprova, por si só, autenticação ou envio efetivo dos dados.
- Os possíveis defeitos identificados devem ser documentados separadamente em `docs/relatorio-de-defeitos.md`.
- Os resultados esperados devem ser revisados caso sejam encontrados requisitos oficiais da aplicação.