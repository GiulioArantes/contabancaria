# 🏦 Banco do Brazil com Z
Sistema de gerenciamento bancário em **Java**, desenvolvido com base nos princípios de **Programação Orientada a Objetos (POO)**. A aplicação simula as funcionalidades básicas de um banco, com suporte para contas correntes e poupança, realizando operações como criação de contas, movimentações financeiras e atualizações cadastrais.

![banco pic](https://i.postimg.cc/xTrZ0BTM/brazilcz.png)

## 🚀 Funcionalidades

* 🏗️ Criação de contas (corrente ou poupança)
* 📃 Listagem de todas as contas
* 🔍 Busca de conta por número
* ✏️ Atualização dos dados da conta
* 🗑️ Remoção de contas
* 💸 Saque e depósito
* 🔁 Transferência entre contas

## 🧠 Conceitos aplicados
* Programação Orientada a Objetos (POO)
* Herança e Polimorfismo (`ContaCorrente` e `ContaPoupanca`)
* Classes abstratas e interfaces
* Encapsulamento com getters e setters
* Organização por camadas: `model`, `controller`, `repository`, `util`
* Manipulação de coleções com `ArrayList`
* Cores no terminal com ANSI (classe `Cores`)
* Validação e tratamento de exceções (`try/catch` e `InputMismatchException`)

## 🧩 Estrutura das Entidades

🔹 **Conta (abstract)**

| Atributo  | Tipo   | Descrição                                  |
| --------- | ------ | ------------------------------------------ |
| `numero`  | int    | Identificador único da conta               |
| `agencia` | int    | Número da agência bancária                 |
| `tipo`    | int    | Tipo da conta (1 = Corrente, 2 = Poupança) |
| `titular` | String | Nome do titular da conta                   |
| `saldo`   | float  | Saldo atual da conta                       |

---

🔸 **ContaCorrente (extends Conta)**

| Atributo | Tipo  | Descrição         |
| -------- | ----- | ----------------- |
| `limite` | float | Limite de crédito |

✔️ Permite saque com uso do limite adicional.

---

🔸 **ContaPoupanca (extends Conta)**
| Atributo      | Tipo | Descrição                            |
| ------------- | ---- | ------------------------------------ |
| `aniversario` | int  | Dia do mês para aniversário da conta |

✔️ Armazena a data para aplicação de rendimentos (simulado).

📂 Estrutura do Projeto
```shell
├── conta/
│   ├── controller/
│   │   └── ContaController.java        # Lógica de controle e operações
│   │
│   ├── model/
│   │   ├── Conta.java                  # Classe abstrata base
│   │   ├── ContaCorrente.java         # Conta com limite
│   │   └── ContaPoupanca.java         # Conta com aniversário
│   │
│   ├── repository/
│   │   └── ContaRepository.java       # Interface de operações CRUD e financeiras
│   │
│   └── util/
│       └── Cores.java                 # Códigos ANSI para colorir o terminal
│
└── Menu.java                          # Classe principal com menu interativo
```

## ▶️ Como executar

1. Clone o repositório
2. Importe o projeto em sua IDE Java (Eclipse, IntelliJ, VSCode...)
3. Execute a classe Menu.java
4. Utilize o terminal para interagir com o menu e testar as funcionalidades

## 💡 Possíveis melhorias futuras

* Persistência de dados com banco (JDBC ou JPA)
* Interface gráfica (Swing ou JavaFX)
* Salvamento local em arquivos
* Geração de relatórios
* Autenticação e login com senha

## 🤝 Contribuição

Contribuições são sempre bem-vindas! Você pode colaborar das seguintes formas:

💡 **Sugestões e feedbacks:** Entre em contato via [LinkedIn](https://www.linkedin.com/in/giulio-arantes/) ou por e-mail: [giulio.arantes@icloud.com](giulio.arantes@icloud.com) </br>
🔧 **Código:** Fork este repositório, implemente melhorias e envie um Pull Request.

> Vamos evoluir juntos como desenvolvedores e criar projetos que façam sentido! 💙
