# Plano de Testes — Web Quality Lab

## 1. Identificação do projeto

**Projeto:** Web Quality Lab  
**Tipo de teste:** Testes funcionais manuais  
**Aplicação sob teste:** [QA Practice Website](https://qaengineerwaqas.com/qa-practice)  
**Status do projeto:** Em andamento

## 2. Objetivo

Definir a estratégia para executar testes funcionais manuais em uma aplicação web, verificando o comportamento dos formulários de login e contato.

O projeto tem como objetivo praticar técnicas de teste de software, documentar resultados reais, identificar comportamentos inesperados e elaborar relatórios de defeitos como parte de um portfólio de QA Júnior.

## 3. Escopo dos testes

### 3.1. Funcionalidades incluídas

**Login**
- Verificar o comportamento com os campos preenchidos.
- Verificar a validação com o campo de e-mail vazio.
- Verificar a validação com o campo de senha vazio.
- Testar e-mails em formatos inválidos.
- Observar o comportamento com credenciais fictícias.

**Formulário de contato**
- Verificar o envio com todos os campos vazios.
- Verificar o envio com preenchimento parcial.
- Verificar o envio com todos os campos preenchidos com dados fictícios em formato válido.

### 3.2. Fora do escopo

Nesta etapa, não fazem parte do projeto:
- Testes automatizados.
- Testes de carga e desempenho.
- Testes de segurança aprofundados.
- Verificação do código-fonte ou da lógica interna do servidor.
- Confirmação de gravação de dados no banco de dados.

## 4. Estratégia de teste

Os testes são executados manualmente, seguindo passos definidos e registrando o comportamento observado na aplicação.

Para cada cenário, são documentados:
- Identificador do caso de teste.
- Objetivo.
- Pré-condições, quando aplicáveis.
- Dados utilizados.
- Passos executados.
- Resultado esperado.
- Resultado obtido.
- Status e observações.

Quando um comportamento inesperado é identificado, ele é analisado e, se pertinente, documentado separadamente no relatório de defeitos.

## 5. Ambiente de teste

**Aplicação:** QA Practice Website  
**URL:** https://qaengineerwaqas.com/qa-practice  
**Tipo de execução:** Manual  
**Ferramentas de documentação:** Visual Studio Code, Markdown e Git  
**Versionamento e publicação:** Git e GitHub  
**Dados utilizados:** Dados fictícios, sem uso de credenciais pessoais.

## 6. Critérios de entrada

Os testes podem ser iniciados quando:
- A aplicação está acessível.
- A funcionalidade a ser testada pode ser acessada.
- Os dados necessários para o cenário foram definidos.
- Os passos do teste estão claros.

## 7. Critérios de saída

A etapa de testes será considerada documentada quando:
- Os cenários planejados tiverem seus resultados registrados.
- Os comportamentos inesperados relevantes estiverem descritos.
- Os possíveis defeitos tiverem passos de reprodução e evidências, quando disponíveis.
- Os documentos do projeto estiverem revisados e consistentes.

Esses critérios indicam conclusão da documentação da etapa, não necessariamente ausência de defeitos na aplicação.

## 8. Critérios para registro de defeitos

Um comportamento inesperado será avaliado considerando:
- O resultado esperado para a funcionalidade.
- O resultado efetivamente observado.
- A possibilidade de reproduzir o comportamento.
- O impacto potencial para o usuário.
- As evidências disponíveis.

Quando não houver requisitos oficiais ou informações suficientes para confirmar a falha, o registro será classificado como comportamento suspeito ou em investigação, evitando conclusões sem evidências.

## 9. Resultados preliminares

Durante a execução dos testes, foram observados dois comportamentos que merecem investigação:

- **BUG-001 — Login:** a aplicação exibiu `Login successful!` em diferentes tentativas com dados fictícios, inclusive com e-mail em formato inválido. Não houve redirecionamento nem abertura de área interna.
- **BUG-002 — Formulário de contato:** a aplicação exibiu `Submitted! (Bug: no validation)` nos cenários com todos os campos vazios, preenchimento parcial e preenchimento completo.

Essas observações não comprovam, por si só, que houve autenticação ou envio efetivo dos dados. Os comportamentos foram registrados para investigação adicional.

## 10. Documentos relacionados

- `README.md` — apresentação geral do projeto.
- `docs/casos-de-teste.md` — cenários executados e resultados observados.
- `docs/relatorio-de-defeitos.md` — documentação dos comportamentos suspeitos identificados.

## 11. Status atual

**Fase:** Execução manual e documentação dos testes.  
**Próxima etapa:** Revisar os documentos, organizar as evidências e preparar o projeto para apresentação no portfólio de QA Júnior.