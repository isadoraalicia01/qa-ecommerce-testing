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
| Resultado obtido | A preencher durante a execução. |
| Status | Não executado. |

### CT002 — Login com senha inválida

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema impede o acesso quando a senha está incorreta. |
| Pré-condições | Aplicação acessível. |
| Dados de teste | standard_user / senha_incorreta |
| Passos | 1. Acessar a página inicial. 2. Informar um usuário válido. 3. Informar uma senha incorreta. 4. Clicar em Login. |
| Resultado esperado | O sistema deve impedir o acesso e apresentar uma mensagem de erro. |
| Resultado obtido | A preencher durante a execução. |
| Status | Não executado. |

### CT003 — Login com campos vazios

| Campo | Descrição |
|---|---|
| Objetivo | Verificar o comportamento do sistema quando o usuário tenta realizar login sem preencher os campos. |
| Pré-condições | Aplicação acessível. |
| Dados de teste | Usuário e senha vazios. |
| Passos | 1. Acessar a página inicial. 2. Manter os campos vazios. 3. Clicar em Login. |
| Resultado esperado | O sistema deve impedir o acesso e informar que o campo Username é obrigatório. |
| Resultado obtido | A preencher durante a execução. |
| Status | Não executado. |

### CT004 — Login com usuário inexistente

| Campo | Descrição |
|---|---|
| Objetivo | Verificar se o sistema impede o acesso de usuários não cadastrados. |
| Pré-condições | Aplicação acessível. |
| Dados de teste | usuario_inexistente / secret_sauce |
| Passos | 1. Acessar a página inicial. 2. Informar um usuário inexistente. 3. Informar uma senha. 4. Clicar em Login. |
| Resultado esperado | O sistema deve impedir o acesso e apresentar uma mensagem de erro. |
| Resultado obtido | A preencher durante a execução. |
| Status | Não executado. |
