# Casos de Teste — Web Quality Lab

## CT-001 — Login com e-mail inválido
**Objetivo:** Verificar a validação do formato do e-mail.
**Pré-condição:** Acessar a tela de login.
**Passos:**
1. Informar um valor inválido no campo de e-mail, como `teste@`.
2. Preencher os demais campos conforme necessário para o teste.
3. Acionar o botão de login.
**Resultado esperado:** O sistema deve rejeitar o formato inválido e apresentar uma orientação adequada.
**Resultado real:** A preencher após nova execução.
**Status:** Não executado.

## CT-002 — Cadastro sem senha e confirmação
**Objetivo:** Verificar se os campos obrigatórios são validados.
**Pré-condição:** Acessar a tela de cadastro.
**Passos:**
1. Preencher os demais campos com dados fictícios válidos.
2. Deixar senha e confirmação de senha vazias.
3. Enviar o formulário.
**Resultado esperado:** Se ambos os campos forem obrigatórios, o cadastro deve ser bloqueado com mensagens de validação.
**Resultado real:** A preencher após nova execução.
**Status:** Não executado.

## CT-003 — Envio de contato com todos os campos vazios
**Objetivo:** Verificar a validação dos campos obrigatórios e a mensagem apresentada.
**Pré-condição:** Acessar o formulário de contato.
**Passos:**
1. Deixar todos os campos vazios.
2. Acionar o botão de envio.
3. Registrar a resposta apresentada, exatamente como exibida.
**Resultado esperado:** Se os campos forem obrigatórios, o envio deve ser bloqueado e devem ser apresentadas orientações adequadas, sem mensagem enganosa de sucesso.
**Resultado real:** A preencher após nova execução.
**Status:** Não executado.
