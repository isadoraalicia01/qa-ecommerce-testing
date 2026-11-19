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

## 3. Casos de teste — Catálogo de produtos

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
| Status | Aprovado. |

### CT007 — Ordenação por nome (A–Z)

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se os produtos são ordenados alfabeticamente em ordem crescente. |
| Pré-condições | Usuário autenticado e catálogo disponível. |
| Passos | 1. Localizar o campo de ordenação. 2. Selecionar Name (A to Z). 3. Verificar a sequência dos produtos. |
| Resultado esperado | Os produtos devem ser apresentados em ordem alfabética crescente. |
| Resultado obtido | Ordenação A-Z correta. |
| Status | Aprovado. |

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

## 4. Observações — Catálogo de produtos

Durante a execução dos testes do catálogo, foi identificada uma possível inconsistência na nomenclatura de um dos produtos.

**Produto identificado:** Test.allTheThings() T-Shirt (Red).

**Descrição:** O nome do produto apresenta uma nomenclatura diferente dos demais itens do catálogo, podendo causar estranheza durante a visualização e análise da ordenação alfabética.

**Observação:** A ocorrência foi registrada para análise, sem reprovação automática dos testes de ordenação.

## 5. Carrinho 

### CT011 — Adicionar produto do carrinho

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema permite adicionar um item e se o contador do carrinho atualiza. |
| Pré-condições | Usuário autenticado e catálogo disponível. |
| Passos | 1. Localizar o produto desejado. 2. Clicar no botão "Add to cart". 3. Observar o ícone do carrinho no canto superior direito e o botão do produto. |
| Resultado esperado | O ícone do carrinho deve exibir uma badge com o número "1", e o botão do produto deve mudar para "Remove". |
| Resultado obtido | Item adicionado e contador atualizado para 1. |
| Status | Aprovado. |

### CT012 — Remover produto do carrinho

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se é possível remover um item previamente adicionado e se o contador atualiza. |
| Pré-condições | Usuário autenticado e com pelo menos um produto adicionado ao carrinho. |
| Passos | 1. Clicar no ícone do carrinho para acessar a página "Your Cart. 2. Localizar o produto na lista. 3. Clicar no botão "Remove". |
| Resultado esperado | O produto deve sumir da lista do carrinho e a badge numérica do ícone do carrinho deve desaparecer. |
| Resultado obtido |Produto removido da lista e badge do carrinho apagada. |
| Status | Aprovado. |

### CT013 — Esvaziamento do carrinho após a compra

| Campo | Descrição |
|---|---|
| Objetivo | Garantir que o carrinho seja esvaziado automaticamente após a conclusão de um pedido. |
| Pré-condições | Pedido recém-finalizado (tela "Checkout: Complete!"). |
| Passos | 1. Na tela de sucesso, clicar no botão "Back Home". 2. Observar o ícone do carrinho no canto superior direito. |
| Resultado esperado | O carrinho de compras não deve exibir nenhuma badge numérica, indicando que está vazio. |
| Resultado obtido | Carrinho exibido sem itens e sem badge numérica. |
| Status | Aprovado. |

## 6. Processo de Checkout

### CT014 — Bloqueio de acesso ao checkout sem autenticação

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema impede o acesso direto ao carrinho ou checkout para usuários não logados. |
| Pré-condições | Usuário deslogado do sistema. |
| Passos | 1. Copiar a URL da página de checkout. 2. Fazer logout do sistema (ou abrir uma aba anônima). 3. Colar a URL e tentar acessar diretamente. |
| Resultado esperado | O sistema deve bloquear o acesso e redirecionar o usuário para a tela de login. |
| Resultado obtido | Acesso bloqueado e redirecionamento para login realizado com sucesso. |
| Status | Aprovado. |

### CT015 — Validação de formato e limite de caracteres no formulário de entrega

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema valida corretamente o tamanho e o formato dos dados inseridos no checkout. |
| Pré-condições | Usuário logado, com produto no carrinho, na tela "Checkout: Your Information". |
| Passos | 1. Inserir "A" no campo First Name. 2. Inserir "B" no campo Last Name. 3. Inserir "1" no campo Zip/Postal Code. 4. Clicar em "Continue". |
| Resultado esperado | O sistema deve bloquear o avanço e exibir mensagens de erro informando que o nome é muito curto e o CEP está em formato inválido. |
| Resultado obtido | O sistema aceitou os dados inválidos e avançou para a tela de resumo do pedido. |
| Status | Reprovado (Bug encontrado). |

### CT016 — Cálculo de frete no resumo do pedido 

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema calcula e adiciona o valor do frete ao total do pedido com base no CEP informado. |
| Pré-condições | Usuário na tela "Checkout: Overview" após inserir um CEP válido. |
| Passos | 1. Chegar à tela de revisão do pedido. 2. Observar o campo de valores (Item total, Tax/Frete e Total). |
| Resultado esperado | O sistema deve apresentar um valor de frete (Shipping) calculado dinamicamente ou fixo, somando-o ao "Item total". |
| Resultado obtido | O sistema não apresenta cobrança de frete (Shipping: Free Pony Express Delivery) independentemente do CEP inserido. |
| Status | Reprovado (Regra de negócio ausente ou Bug ). |

## 7. Resumo da execução

| Indicador | Resultado |
|---|---|
| Total de casos executados | 16 |
| Aprovados | 14 |
| Reprovados | 2 |
| Não executados | 0 |

**Conclusão:** A maior parte dos fluxos críticos da aplicação (Login, Listagem de Produtos, Ordenação e Carrinho) foi executada com sucesso e apresentou o comportamento esperado. No entanto, foram identificadas falhas no módulo de Checkout relacionadas à falta de validação dos dados de entrada (nome e CEP) e à ausência de cálculo de frete. Estes dois cenários (CT015 e CT016) foram reprovados e devidamente documentados no relatório de bugs.
