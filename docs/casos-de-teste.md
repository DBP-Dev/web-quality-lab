## CT-001 — Login com campos preenchidos

**Objetivo:** Verificar a resposta da aplicação após o preenchimento dos campos de login.

**Passos executados:**
1. Preencher os campos conforme solicitado pela aplicação.
2. Clicar no botão de login.

**Resultado esperado:** A aplicação deve aceitar os dados somente quando forem válidos, conforme as regras de autenticação.

**Resultado obtido:** A mensagem `Login successful!` foi exibida.

**Status:** Executado — comportamento a investigar.

---

## CT-002 — Login com e-mail vazio

**Objetivo:** Verificar se a aplicação valida o preenchimento do e-mail.

**Passos executados:**
1. Deixar o campo de e-mail vazio.
2. Preencher o campo de senha.
3. Clicar no botão de login.

**Resultado esperado:** A aplicação deve impedir o envio e informar que todos os campos obrigatórios precisam ser preenchidos.

**Resultado obtido:** A mensagem `Preencha todos os campos` foi exibida.

**Status:** Executado — validação observada.


## CT-003 — Login com senha vazia

**Objetivo:** Verificar se a aplicação valida o preenchimento do campo de senha.

**Pré-condição:** Estar na tela de login.

**Passos executados:**
1. Preencher o campo de e-mail.
2. Deixar o campo de senha vazio.
3. Clicar no botão de login.

**Resultado esperado:** A aplicação deve impedir o login e informar que os campos obrigatórios precisam ser preenchidos.

**Resultado obtido:** A mensagem `Preencha todos os campos` foi exibida.

**Status:** Executado — validação observada.

## CT-004 — Login com e-mail em formato inválido

**Objetivo:** Verificar se a aplicação valida o formato do e-mail informado no login.

**Pré-condição:** Estar na tela de login da aplicação.

**Dados de teste:**
- E-mail: `teste@`
- Senha: `SenhaTeste123` (senha fictícia)

**Passos executados:**
1. Acessar a tela de login.
2. Informar `teste@` no campo de e-mail.
3. Informar uma senha fictícia no campo de senha.
4. Clicar no botão de login.
5. Observar a mensagem exibida e verificar se ocorre redirecionamento.

**Resultado esperado:** A aplicação deve rejeitar o formato inválido do e-mail e não informar que o login foi bem-sucedido.

**Resultado obtido:** A aplicação exibiu a mensagem `Login successful!`. Não houve redirecionamento nem abertura de uma área interna.

**Status:** Executado — possível defeito em investigação.

**Observação:** A mensagem de sucesso, isoladamente, não comprova que a autenticação foi realizada. É necessário investigar o comportamento da aplicação antes de confirmar o defeito.

## CT-005 — Login com credenciais fictícias em formato válido

**Objetivo:** Verificar o comportamento do login quando são informados um e-mail em formato válido e uma senha fictícia.

**Pré-condição:** Estar na tela de login da aplicação. O site não disponibiliza credenciais de teste.

**Dados de teste:**
- E-mail: `teste@example.com`
- Senha: `SenhaTeste123`

**Passos executados:**
1. Acessar a tela de login.
2. Preencher o campo de e-mail com `teste@example.com`.
3. Preencher o campo de senha com `SenhaTeste123`.
4. Clicar no botão de login.
5. Observar a mensagem exibida e verificar se ocorre redirecionamento.

**Resultado esperado:** Sem credenciais de teste válidas fornecidas pelo site, não é possível definir com certeza o resultado esperado para a autenticação. Como medida de segurança, credenciais inválidas não devem resultar em autenticação bem-sucedida.

**Resultado obtido:** A aplicação exibiu a mensagem `Login successful!`, mas não houve redirecionamento nem abertura de uma área interna.

**Status:** Executado — comportamento suspeito em investigação.

**Observação:** O resultado é semelhante ao observado no CT-004. É necessário investigar se a mensagem representa uma autenticação real ou apenas uma resposta visual da interface.