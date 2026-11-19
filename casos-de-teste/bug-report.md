# Relatório de Bugs (Bug Report)

Este documento contém o registro das falhas encontradas durante a execução dos Casos de Teste no módulo de Checkout.

---

## Bug 001: Validação ausente nos campos do formulário de entrega (Checkout)

**ID do Caso de Teste associado:** CT015
**Status:** Aberto 
**Severidade:** Alta
**Prioridade:** Média

### Descrição
O formulário de informações de entrega (`Checkout: Your Information`) não possui validação de quantidade mínima de caracteres e nem formato de dados (Regex). O sistema está permitindo o avanço para a página de revisão do pedido com nomes de apenas 1 letra e CEP de 1 dígito.

### Passos para Reproduzir
1. Faça login na aplicação com um usuário válido (ex: `standard_user`).
2. Adicione qualquer produto ao carrinho.
3. Acesse o carrinho e clique no botão **"Checkout"**.
4. No campo **First Name**, digite a letra `"A"`.
5. No campo **Last Name**, digite a letra `"B"`.
6. No campo **Zip/Postal Code**, digite o número `"1"`.
7. Clicar no botão **"Continue"**.

### Resultado Esperado
O sistema deveria bloquear o avanço, destacando os campos em vermelho e exibindo uma mensagem de erro informando que os dados inseridos são inválidos (ex: "O nome deve conter no mínimo 2 caracteres", "Formato de CEP inválido").

### Resultado Atual (Obtido)
O sistema aceita os dados de 1 caractere como válidos, não exibe nenhuma mensagem de erro e redireciona o usuário indevidamente para a página de resumo do pedido (`Checkout: Overview`).

### Evidências
<img width="927" height="709" alt="image" src="https://github.com/user-attachments/assets/65441d82-a17e-4fd4-bd94-551c434d779e" />
<img width="927" height="709" alt="CT015-formulario-de-entrega-02" src="https://github.com/user-attachments/assets/eb491f22-8699-42dd-b2c1-26e753020670" />

---

## Bug 002: Ausência de cálculo de frete baseado no CEP (Regra de Negócio)

**ID do Caso de Teste associado:** CT016
**Status:** Aberto 
**Severidade:** Média
**Prioridade:** Baixa

### 📝 Descrição
Ao avançar para a tela de revisão do pedido (`Checkout: Overview`), o sistema exibe um frete fixo (`Shipping: Free Pony Express Delivery`) independentemente do número de CEP que foi informado na etapa anterior. 

*(Siga a mesma estrutura de passos, resultado esperado e obtido do Bug 001 para completar este)*
