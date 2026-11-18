# Casos de Teste — E-commerce

## 1. Identificação

| Informação | Descrição |
|---|---|
| Projeto | Testes de Software em E-commerce |
| Aplicação | SauceDemo |
| Módulo | Login |
| Tipo de teste | Manual e funcional |

## 2. Casos de teste

### CT001 — Login com credenciais válidas

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o usuário consegue acessar o sistema com credenciais válidas. |
| Pré-condições | Aplicação acessível e usuário válido disponível. |
| Dados de teste | standard_user / secret_sauce |
| Passos | 1. Acessar a página inicial. 2. Informar o usuário. 3. Informar a senha. 4. Clicar em Login. |
| Resultado esperado | O sistema deve permitir o acesso e direcionar o usuário para a página de produtos. |
| Resultado obtido | Acessso realizado e página de produtos exibida. |
| Status | Aprovado. |

### CT002 — Login com senha inválida

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema impede o acesso quando a senha está incorreta. |
| Pré-condições | Aplicação acessível. |
| Dados de teste | standard_user / senha_incorreta |
| Passos | 1. Acessar a página inicial. 2. Informar um usuário válido. 3. Informar uma senha incorreta. 4. Clicar em Login. |
| Resultado esperado | O sistema deve impedir o acesso e apresentar uma mensagem de erro. |
| Resultado obtido | Acesso bloqueado e mensagem de erro apresentada. |
| Status | Aprovado. |

### CT003 — Login com campos vazios

| Campo | Descrição |
|---|---|
| Objetivo | Verificar o comportamento do sistema quando o usuário tenta realizar login sem preencher os campos. |
| Pré-condições | Aplicação acessível. |
| Dados de teste | Usuário e senha vazios. |
| Passos | 1. Acessar a página inicial. 2. Manter os campos vazios. 3. Clicar em Login. |
| Resultado esperado | O sistema deve impedir o acesso e informar que o campo Username é obrigatório. |
| Resultado obtido | Acesso bloqueado e mensagem de campo obrigatório apresentada. |
| Status | Aprovado. |

### CT004 — Login com usuário inexistente

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema impede o acesso de usuários não cadastrados. |
| Pré-condições | Aplicação acessível. |
| Dados de teste | usuario_inexistente / secret_sauce |
| Passos | 1. Acessar a página inicial. 2. Informar um usuário inexistente. 3. Informar uma senha. 4. Clicar em Login. |
| Resultado esperado | O sistema deve impedir o acesso e apresentar uma mensagem de erro. |
| Resultado obtido | Acesso bloqueado e mensagem de erro apresentada. |
| Status | Aprovado. |

## 3. Resumo da execução

| Indicador | Resultado |
|---|---|
| Total de casos executados | 4 |
| Aprovados | 4 |
| Reprovados | 0 |
| Não executados | 0 |

**Conclusão:** Todos os casos de teste relacionados ao módulo de login foram executados com sucesso. O comportamento observado correspondeu aos resultados esperados.

## 4. Casos de teste — Catálogo de produtos

### CT005 — Exibição da lista de produtos

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se a página apresenta corretamente os produtos disponíveis. |
| Pré-condições | Usuário autenticado no sistema. |
| Passos | 1. Acessar a página de produtos. 2. Verificar se os produtos são exibidos. |
| Resultado esperado | O sistema deve apresentar os produtos com nome, imagem, descrição e preço. |
| Resultado obtido | Exibição de produtos correta. |
| Status | Aprovado. |

### CT006 — Quantidade de produtos exibidos

| Campo | Descrição |
|---|---|
| Objetivo | Verificar a quantidade de produtos disponíveis no catálogo. |
| Pré-condições | Usuário autenticado no sistema. |
| Passos | 1. Acessar a página de produtos. 2. Contar os produtos apresentados. |
| Resultado esperado | O catálogo deve apresentar 6 produtos. |
| Resultado obtido | Quantidade de produtos correta. |
| Status | Não executado. |

### CT007 — Ordenação por nome (A–Z)

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se os produtos são ordenados alfabeticamente em ordem crescente. |
| Pré-condições | Usuário autenticado e catálogo disponível. |
| Passos | 1. Localizar o campo de ordenação. 2. Selecionar Name (A to Z). 3. Verificar a sequência dos produtos. |
| Resultado esperado | Os produtos devem ser apresentados em ordem alfabética crescente. |
| Resultado obtido | A camiseta Test.allTheThings() T-Shirt (Red) aparece por último, apesar de começar com T. |
| Status | Reprovado. |

### CT008 — Ordenação por nome (Z–A)

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se os produtos são ordenados alfabeticamente em ordem decrescente. |
| Pré-condições | Usuário autenticado e catálogo disponível. |
| Passos | 1. Localizar o campo de ordenação. 2. Selecionar Name (Z to A). 3. Verificar a sequência dos produtos. |
| Resultado esperado | Os produtos devem ser apresentados em ordem alfabética decrescente. |
| Resultado obtido | Ordenação Z-A correta. |
| Status | Aprovado. |

### CT009 — Ordenação por preço (menor para maior)

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se os produtos são ordenados pelo preço em ordem crescente. |
| Pré-condições | Usuário autenticado e catálogo disponível. |
| Passos | 1. Localizar o campo de ordenação. 2. Selecionar Price (low to high). 3. Verificar a sequência dos preços. |
| Resultado esperado | Os produtos devem ser apresentados do menor para o maior preço. |
| Resultado obtido | Preço crescente correto. |
| Status | Aprovado. |

### CT010 — Ordenação por preço (maior para menor)

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se os produtos são ordenados pelo preço em ordem decrescente. |
| Pré-condições | Usuário autenticado e catálogo disponível. |
| Passos | 1. Localizar o campo de ordenação. 2. Selecionar Price (high to low). 3. Verificar a sequência dos preços. |
| Resultado esperado | Os produtos devem ser apresentados do maior para o menor preço. |
| Resultado obtido | Preço decrescente correto. |
| Status | Aprovado. |

## 5. Observações — Catálogo de produtos

Durante a execução dos testes do catálogo, foi identificada uma possível inconsistência na nomenclatura de um dos produtos.

**Produto identificado:** Test.allTheThings() T-Shirt (Red).

**Descrição:** O nome do produto apresenta uma nomenclatura diferente dos demais itens do catálogo, podendo causar estranheza durante a visualização e análise da ordenação alfabética.

**Observação:** A ocorrência foi registrada para análise, sem reprovação automática dos testes de ordenação.
