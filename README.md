# Trybank

## Descrição do Projeto
Bem-vindo ao repositório do projeto Trybank! Este projeto consiste na criação de uma aplicação bancária para gerenciar contas, realizando operações como checar saldo, depositar, sacar e transferir dinheiro. Além disso, o sistema permite o cadastro, login e logout de usuários.

### Habilidades Técnicas Desenvolvidas
Neste projeto, foram aplicadas as seguintes habilidades:

- **Entendimento de Estruturas de Array**
- **Conversão e Manipulação de Variáveis de Diversos Tipos**
- **Operações Aritméticas**
- **Construção de Algoritmos com Estruturas de Controle**
- **Lançamento de Exceções Controladas**

## Requisitos do Projeto

### 1. Cadastro de Novas Contas
Na função `RegisterAccount()`, o programa permite o cadastro de novas contas. Se a combinação de número e agência já existir, uma exceção do tipo ArgumentException é lançada com a mensagem "A conta já está sendo usada!". Caso contrário, os dados são armazenados no array `Bank` na próxima posição disponível, marcada por `registeredAccounts` com saldo 0.

### 2. Login
Na função `Login()`, o programa permite o login do usuário. Se já houver uma pessoa usuária logada, é lançada uma exceção do tipo AccessViolationException com a mensagem "Usuário já está logado". Se a combinação de número e agência é encontrada e a senha é correta, o estado da variável `Logged` é alterado, e a posição da pessoa usuária logada é armazenada em `loggedUser`. Se a senha estiver incorreta, é lançada uma exceção do tipo ArgumentException com a mensagem "Senha incorreta". Se a combinação não for encontrada, é lançada uma exceção do tipo ArgumentException com a mensagem "Agência + Conta não encontrada".

### 3. Logout
Na função `Logout()`, o programa permite o logout do usuário. Se não houver uma pessoa usuária logada, é lançada uma exceção do tipo AccessViolationException com a mensagem "Usuário não está logado". Caso contrário, o estado da variável `Logged` é alterado, e o índice de pessoa usuária `loggedUser` é resetado para -99.

### 4. Checar Saldo
Na função `CheckBalance()`, o programa permite verificar o saldo na conta da pessoa usuária logada. Se não houver uma pessoa usuária logada, é lançada uma exceção do tipo AccessViolationException com a mensagem "Usuário não está logado". Caso contrário, a função retorna o saldo na conta da pessoa usuária logada.

### 5. Depositar Dinheiro
Na função `Deposit()`, o programa permite o depósito de um valor na conta da pessoa usuária logada. Se não houver uma pessoa usuária logada, é lançada uma exceção do tipo AccessViolationException com a mensagem "Usuário não está logado". Caso contrário, o valor é adicionado ao saldo da pessoa usuária logada.

### 6. Sacar Dinheiro
Na função `Withdraw()`, o programa permite o saque de um valor na conta da pessoa usuária logada. Se não houver uma pessoa usuária logada, é lançada uma exceção do tipo AccessViolationException com a mensagem "Usuário não está logado". Caso contrário, o valor é retirado do saldo da pessoa usuária logada. Se o saldo for insuficiente, é lançada uma exceção do tipo InvalidOperationException com a mensagem "Saldo insuficiente".

### 7. Transferir Dinheiro entre Contas
Na função `Transfer(int destinationNumber, int destinationAgency, int value)`, o programa permite a transferência de saldo entre uma pessoa usuária logada e uma conta existente. Se não houver uma pessoa usuária logada, é lançada uma exceção do tipo AccessViolationException com a mensagem "Usuário já está logado". Se o saldo da conta da pessoa usuária logada for insuficiente, é lançada uma exceção do tipo InvalidOperationException com a mensagem "Saldo insuficiente". Caso contrário, o valor é transferido do saldo da pessoa usuária logada para o saldo da conta destino.

## Habilidades Técnicas

- **Linguagens:**
  - C#


- **Outras Habilidades:**
  - Manipulação de arrays multidimensionais
  - Lançamento e tratamento de exceções
  - Separação de responsabilidades no código
  - Construção de métodos para implementação gradual dos requisitos.
