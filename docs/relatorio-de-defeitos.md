# Relatório de Defeitos — Web Quality Lab

## BUG-001 — Login: a mensagem Login successful! aparece até com dados inválidos, mas não ocorre redirecionamento.

**Resumo:** A tela de login exibe a mensagem `Login successful!` independentemente dos dados informados nos campos de e-mail e senha.

**Ambiente:** QA Practice Website — https://qaengineerwaqas.com/qa-practice

**Pré-condição:** Estar na tela de login.

**Passos para reproduzir:**
1. Acessar a tela de login.
2. Informar diferentes combinações de e-mail e senha, incluindo dados em formatos inválidos e dados fictícios em formatos aparentemente válidos.
3. Clicar no botão de login em cada tentativa.
4. Observar a mensagem apresentada e o comportamento da tela.

**Resultado esperado:** A aplicação deve validar os dados de autenticação e não apresentar uma mensagem de sucesso quando as credenciais forem inválidas.

**Resultado obtido:** Segundo os testes executados, a aplicação exibe `Login successful!` independentemente dos dados informados. Não ocorre redirecionamento nem abertura de uma área interna.

**Impacto potencial:** A mensagem pode induzir o usuário a acreditar que a autenticação foi realizada com sucesso, mesmo quando isso não foi demonstrado.

**Severidade:** A definir após investigação adicional.

**Prioridade:** A definir conforme o impacto confirmado.

**Status:** Em investigação.


**Evidência:**
![BUG-001 — Mensagem de sucesso no login](../evidencias/BUG-001-login-sucesso.png)

**Observação:** Não foi possível confirmar se a autenticação é realmente realizada. O defeito observado, até o momento, é o comportamento da mensagem de sucesso. A lógica interna de autenticação não foi verificada.

## BUG-002 — Formulário de contato: aparece Submitted! (Bug: no validation) mesmo com os campos vazios ou parcialmente preenchidos.

**Resumo:** O formulário de contato exibe a mensagem `Submitted! (Bug: no validation)` independentemente do preenchimento dos campos.

**Ambiente:** QA Practice Website — https://qaengineerwaqas.com/qa-practice

**Pré-condição:** Estar na seção do formulário de contato.

**Cenários executados:**
- **CT-005:** Envio com todos os campos vazios.
- **CT-006:** Envio preenchendo somente os campos de nome e mensagem.
- **CT-007:** Envio com todos os campos preenchidos com dados fictícios em formato válido.

**Passos para reproduzir:**
1. Acessar o formulário de contato.
2. Preparar um dos cenários de preenchimento descritos acima.
3. Clicar no botão de envio.
4. Observar a mensagem apresentada.
5. Repetir o procedimento com os outros dois cenários.

**Resultado esperado:** Se os campos forem obrigatórios, a aplicação deve impedir o envio quando estiverem vazios ou incompletos e informar quais campos precisam ser corrigidos. Quando os dados forem válidos, deve apresentar uma confirmação de envio apropriada.

**Resultado obtido:** Nos três cenários, a aplicação exibiu a mesma mensagem: `Submitted! (Bug: no validation)`.

**Impacto potencial:** O formulário pode aceitar tentativas de envio com dados obrigatórios ausentes e não diferenciar entradas completas de incompletas.

**Severidade:** A definir após verificar os requisitos e o comportamento esperado.

**Prioridade:** A definir.

**Status:** Comportamento reproduzido — validação em investigação.

**Evidência:** 
![BUG-002 - Mensagem do formulario de contato](../evidencias/BUG-002-formulario-sem-validacao.png)

**Observação:** A mensagem sugere ausência de validação, mas não comprova que os dados foram efetivamente enviados ou armazenados. Essa parte não foi verificada.