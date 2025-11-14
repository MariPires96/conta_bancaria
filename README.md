# 🏦 Sistema de Contas Bancárias em Memória

Projeto desenvolvido em **TypeScript** como exercício de Programação Orientada a Objetos (POO), simulando um sistema básico de gerenciamento de contas bancárias. O sistema utiliza um **Array em memória** para persistência temporária dos dados.

## ⚙️ Status do Projeto

✅ **Camadas Essenciais e Lógica Bancária Completa**

---

## 💡 Funcionalidades Implementadas

A aplicação oferece as seguintes funcionalidades, todas implementadas na camada de controle (`ContaController`):

### Operações Bancárias Principais:

* **Sacar:** Implementação da lógica de saque, incluindo validações.
* **Depositar:** Implementação da lógica de depósito.
* **Transferir:** Implementação da lógica completa de transferência entre contas.

### Operações CRUD e Auxiliares:

* **Listar Todas:** Exibe todas as contas cadastradas (`listaContas`).
* **Buscar Conta:** Localiza uma conta específica pelo seu número.
* **Gerar Número da Conta:** Método auxiliar para controle de Chave Primária (*auto-increment*).
* **Armazenamento em Memória:** Utiliza um Array (`listaContas`) para simular o banco de dados.

---

## 📐 Arquitetura do Projeto (POO)

A aplicação segue uma arquitetura baseada em camadas, utilizando os seguintes conceitos de POO para garantir padronização e manutenibilidade:

| Camada | Conceito POO | Descrição |
| :--- | :--- | :--- |
| **Modelo** | **Classe Abstrata (`Conta`)** | Define a base abstrata para padronizar e obrigar a implementação de métodos essenciais nas classes filhas (`ContaCorrente`, `ContaPoupanca`). |
| **Persistência** | **Interface (`ContaRepository`)** | Define o contrato de serviço, obrigando a classe implementadora a fornecer a assinatura de todos os métodos de manipulação de contas (CRUD e bancários). |
| **Controladora** | **Implementação Concreta (`ContaController`)** | Classe que **implementa** a `ContaRepository` e contém toda a lógica de negócio e manipulação direta do Array de Contas. |

---

## 🚀 Como Executar o Projeto

Assumindo que você tem o Node.js e o TypeScript configurados, siga os passos para rodar o projeto localmente:

1.  **Clone o repositório:**
    ```bash
    git clone [SUA URL DO REPOSITÓRIO AQUI]
    ```
2.  **Entre na pasta do projeto:**
    ```bash
    cd nome-do-seu-projeto
    ```
3.  **Instale as dependências:**
    ```bash
    npm install
    ```
4.  **Execute o projeto:** (Use o comando configurado no seu `package.json` ou `ts-node`)
    ```bash
    npm start 
    ```

