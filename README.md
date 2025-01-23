# Sistema de Gerenciamento de Conta Corrente

Este projeto implementa um sistema básico de gerenciamento de contas correntes utilizando JavaScript. Ele permite criar contas, realizar saques, depósitos, e consultar o saldo, incluindo suporte para contas comuns e contas especiais com limite de crédito.

---

## Funcionalidades

1. **Abertura de Conta**:
   - Permite criar uma conta comum ou especial.
   - Contas comuns não possuem limite de crédito.
   - Contas especiais incluem a definição de um limite de crédito.

2. **Saque**:
   - Realiza saques da conta, observando se há saldo suficiente.
   - Para contas especiais, é possível usar o limite de crédito, com alertas sobre seu uso.

3. **Depósito**:
   - Adiciona valores ao saldo da conta.

4. **Impressão de Extrato**:
   - Exibe o saldo atual da conta e o limite de crédito (se aplicável).

5. **Sair do Sistema**:
   - Finaliza o programa.

---

## Como Utilizar

1. Execute o programa em um ambiente que suporte JavaScript no navegador (como o console do navegador).
2. Navegue pelas opções do menu para realizar as operações:

```
Escolha uma opção:

[1] Abertura de conta corrente.
[2] Saque.
[3] Depósito.
[4] Imprimir extrato.
[5] Sair.
```

---

## Fluxo das Operações

1. **Abertura de Conta**:
   - O programa solicita o número da conta, saldo inicial e tipo de conta (comum ou especial).
   - Caso seja uma conta especial, é necessário informar o limite de crédito.

2. **Saque**:
   - Solicita o valor a ser sacado.
   - Valida se há saldo suficiente:
     - Contas comuns: impede saques que deixariam o saldo negativo.
     - Contas especiais: permite usar o limite de crédito, mas impede exceder o limite.

3. **Depósito**:
   - Solicita o valor a ser depositado e o adiciona ao saldo atual.

4. **Impressão de Extrato**:
   - Exibe o saldo atual e, no caso de contas especiais, o limite de crédito disponível.

5. **Sair**:
   - Finaliza o programa com uma mensagem de despedida.

---

## Estrutura do Código

1. **Função `inicio()`**:
   - Exibe o menu principal e redireciona para a operação escolhida.

2. **Função `operacionar(opcao)`**:
   - Controla o fluxo das operações com base na opção escolhida pelo usuário.

3. **Função `abrirConta()`**:
   - Inicializa os dados da conta (número, saldo inicial, tipo de conta e limite, se aplicável).

4. **Função `sacar(valor)`**:
   - Realiza a operação de saque, com validações para contas comuns e especiais.

5. **Função `depositar(valor)`**:
   - Adiciona um valor ao saldo da conta.

6. **Função `imprimirSaldo(mensagem, valor)`**:
   - Exibe o saldo da conta e o limite (para contas especiais).

---

## Validações Importantes

- Antes de qualquer operação (saque, depósito, ou extrato), o sistema verifica se uma conta foi criada.
- Saques em contas comuns não permitem saldo negativo.
- Saques em contas especiais respeitam o limite de crédito configurado.

---

## Exemplo de Uso

### Cenário 1: Abertura de Conta Especial e Uso do Limite
1. Abertura de conta com saldo inicial de R$ 100,00 e limite de crédito de R$ 200,00.
2. Saque de R$ 250,00:
   - Saldo passa a R$ -150,00 (usando R$ 150,00 do limite de crédito).
3. Impressão de extrato:
   - Mostra saldo atual e limite de crédito restante.

### Cenário 2: Conta Comum
1. Abertura de conta comum com saldo inicial de R$ 50,00.
2. Tentativa de saque de R$ 100,00:
   - Operação bloqueada por saldo insuficiente.

---

## Observação
Este programa utiliza `prompt()` e `alert()` para interação com o usuário, sendo ideal para testes em ambientes simples, como o console de um navegador. Para uma aplicação real, considere adaptar para interfaces modernas (como HTML/CSS) ou APIs de backend.

---

## Contato
Para sugestões ou melhorias, entre em contato: **[guilherme.g.martins@gmail.com]**

