# 🏦 Sistema Bancário em Python

Projeto completo desenvolvido em Python, simulando o funcionamento de um sistema bancário real. Criado com foco em **Programação Orientada a Objetos (POO)**, traz todas as operações principais que encontramos em bancos digitais, com validações de segurança, regras de negócio, organização de dados e interface interativa para o usuário.

🔗 **Repositório:** https://github.com/MS-prog-964/Sistema_bancario

---

## 📋 Sobre o Projeto

O Sistema Bancário foi desenvolvido para simular o dia a dia de uma conta corrente, permitindo ao usuário realizar todas as operações financeiras básicas e avançadas de forma segura e prática. O projeto foi construído utilizando conceitos avançados da linguagem Python, com foco em organização, reutilização de código e tratamento de erros, garantindo um sistema robusto e que não quebra com entradas inválidas.

Todo o código foi estruturado usando Classes e Objetos, o que facilita muito a manutenção e futuras atualizações, seguindo o padrão de projetos de software profissionais. Ele serve tanto para estudo de lógica de programação quanto como base para sistemas maiores de gestão financeira.

---

## ⚙️ Funcionalidades Completas

✅ **Cadastro de Conta e Usuário**: Criação de conta com nome, número da conta único e saldo inicial.
✅ **Operação de Depósito**: Permite adicionar valores à conta, com validação para aceitar apenas valores positivos e válidos.
✅ **Operação de Saque**: Realiza retirada de valores, com **validação automática de saldo** (não deixa sacar mais dinheiro do que tem na conta) e valores permitidos.
✅ **Transferência via PIX**: Funcionalidade completa para enviar valores para **outras contas cadastradas** no sistema, verificando origem, destino e saldo disponível.
✅ **Extrato Detalhado**: Histórico completo de todas as movimentações realizadas (depósitos, saques e transferências), mostrando tipo de operação, valor e saldo atual em tempo real.
✅ **Consulta de Saldo**: Verificação rápida e segura do valor disponível na conta.
✅ **Validação de Dados Blindada**: O sistema não aceita letras, valores negativos ou campos vazios, tratando todos os erros possíveis para não travar o programa.
✅ **Gerenciamento de Múltiplas Contas**: É possível cadastrar e gerenciar várias contas diferentes dentro do mesmo sistema, cada uma com seus dados e saldos separados.
✅ **Menu Interativo**: Interface de texto amigável, com opções numeradas para navegar facilmente entre as funções.
✅ **Identificação Única**: Cada conta recebe um número único automaticamente, evitando duplicidade de cadastro.

---

## 🧮 Regras de Negócio Implementadas

🔹 **Valores de Operação**: Todo valor inserido para depósito, saque ou transferência deve ser **maior que R$ 0,00**. Valores negativos ou zero são bloqueados.
🔹 **Regra de Saldo**: O sistema bloqueia automaticamente qualquer saque ou transferência se o valor for maior que o saldo disponível na conta de origem.
🔹 **Validação de Conta Destino**: Ao fazer uma transferência, o sistema verifica se o número da conta que receberá o dinheiro realmente existe no cadastro.
🔹 **Controle de Extrato**: Toda operação realizada é registrada permanentemente no histórico, não podendo ser apagada, garantindo a confiabilidade dos dados.
🔹 **Identificação**: Número da conta gerado de forma sequencial e única para cada novo usuário cadastrado.

---

## 🚀 Tecnologias e Conceitos Utilizados

- **Python 3.x**: Linguagem principal de desenvolvimento.
- **Programação Orientada a Objetos (POO)**: Uso de Classes, Atributos e Métodos para estruturar o sistema.
- **Métodos Construtores**: Para inicialização correta dos dados de cada conta.
- **Encapsulamento**: Proteção dos dados internos da conta, acessíveis apenas através dos métodos.
- **Tratamento de Erros (`try/except`)**: Sistema blindado contra entradas de dados inválidas (letras, símbolos, valores errados).
- **Estruturas de Repetição e Condicionais**: Controle de fluxo do menu e das regras de negócio.
- **Listas e Dicionários**: Armazenamento e organização dos dados dos usuários e movimentações.
- **Funções e Métodos**: Separação das responsabilidades, deixando o código limpo e organizado.
- **Formatação Monetária**: Valores formatados em Real Brasileiro (R$).

---

## 📂 Estrutura do Projeto

Sistema_bancario/
├── sistema_bancario.py # Arquivo principal com todo o código do sistema
├── README.md           # Documentação completa do projeto
└── (outros arquivos)   # Possíveis arquivos de dados ou versões
 
plaintext
  

### 📄 Detalhamento dos Arquivos:

📌 **sistema_bancario.py**
- Classe `Conta`: Responsável por armazenar os dados do titular, número da conta e saldo. Contém todos os métodos das operações: `depositar()`, `sacar()`, `transferir()` e `exibir_extrato()`.
- Classe `SistemaBancario`: Responsável por gerenciar todas as contas cadastradas, controlar o menu principal e a interação com o usuário.
- Funções de validação: Verificam se os dados inseridos são números, se são positivos e seguem as regras.
- Menu principal: Loop infinito que apresenta as opções até o usuário escolher sair do sistema.

📌 **README.md**
- Esse arquivo que contém toda a explicação, documentação e detalhes técnicos do que foi desenvolvido.

---

## 🖥️ Como Executar o Sistema

1. **Pré-requisito**: Ter o Python instalado na máquina (versão 3.0 ou superior).
2. **Baixar o projeto**: Clone ou baixe os arquivos desse repositório.
```bash
git clone https://github.com/MS-prog-964/Sistema_bancario.git
 
 
3. Acessar a pasta:
 
bash
  
cd Sistema_bancario
 
 
4. Executar o arquivo:
 
bash
  
python sistema_bancario.py
 
 
5. Usar: Seguir as instruções que aparecerão no terminal para navegar pelo menu e realizar as operações.
 
 
 
📊 Fluxo de Funcionamento
 
1. Ao iniciar, o sistema apresenta o menu principal com as opções: Criar Conta, Acessar Conta, Depositar, Sacar, Transferir, Ver Extrato, Sair.
2. Ao criar uma conta, é solicitado o nome do titular e o saldo inicial. O número da conta é gerado automaticamente.
3. Ao escolher qualquer operação financeira, o sistema valida os dados, verifica as regras e executa a ação, mostrando mensagens de sucesso ou erro claras.
4. Todas as alterações de saldo são atualizadas na hora e registradas no extrato.
5. Ao consultar o extrato, é exibido um histórico completo com data, tipo de operação, valor e o saldo final após cada movimento.
 
 
 
📈 Melhorias Futuras
 
Para versões novas do sistema, já estão planejadas:
 
🔹 Sistema de senha e autenticação para cada conta.
🔹 Limite diário para saques e transferências.
🔹 Registro de data e hora automático em cada transação.
🔹 Salvamento dos dados em arquivos externos, para não perder informações ao fechar o programa.
🔹 Empréstimo e rendimento de poupança.
🔹 Interface gráfica visual, além do modo texto atual.
🔹 Relatórios mensais de gastos.
 
 
 
🧠 O que foi aprendido com esse projeto?
 
Esse projeto é um exemplo clássico e completo de como aplicar a Orientação a Objetos na prática. Foi possível praticar:
 
- Como modelar problemas do mundo real em código.
- Como proteger dados e garantir que as regras sejam seguidas.
- Como fazer um código que seja fácil de ler e entender.
- Como tratar erros para deixar o programa profissional.
- Como estruturar um sistema grande dividindo as funções em partes menores.

Desenvolvido por MS-prog-964.
 
🌐 GitHub: https://github.com/MS-prog-964
  
