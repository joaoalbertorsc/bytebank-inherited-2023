### `README.md`

## Sistema de Gerenciamento de Funcionários e Autenticação

Este projeto em Java consiste em um sistema simples de gerenciamento de funcionários, controle de bônus e autenticação. Ele demonstra conceitos de Programação Orientada a Objetos (POO), como herança, polimorfismo e interfaces.

### Tecnologias Utilizadas

* **Java**: A linguagem de programação principal utilizada para desenvolver todas as classes e a lógica do sistema.

### Estrutura do Projeto

O sistema é composto pelas seguintes classes e interfaces:

#### Classes Principais

* `Employee.java`: Classe base para todos os funcionários. Contém atributos como nome, CPF e salário, além de métodos para acesso e modificação desses dados.
* `Adm.java`: Representa um administrador. É uma subclasse de `Employee` e implementa a interface `Authenticable`, permitindo que ele seja autenticado no sistema.
* `Manager.java`: Representa um gerente. Também é uma subclasse de `Employee` e implementa `Authenticable`.
* `Designer.java`: Subclasse de `Employee` que representa um designer.
* `VideoEditor.java`: Subclasse de `Employee` que representa um editor de vídeo.
* `Client.java`: Representa um cliente, que também pode ser autenticado, implementando a interface `Authenticable`.
* `InternalSystem.java`: Classe responsável por gerenciar a autenticação no sistema.
* `Authenticator.java`: Lida com a lógica de autenticação, verificando se uma chave está correta.
* `BonusControl.java`: Classe para controlar a bonificação dos funcionários.

#### Interfaces

* `Authenticable.java`: Define os métodos que uma classe precisa implementar para ser autenticável, como `setKey` (para definir uma chave) e `authentication` (para realizar a autenticação).

### Como Rodar

O projeto consiste em arquivos `.class` compilados a partir de um código-fonte Java. Para executar os testes e ver o sistema em ação, você pode usar a linha de comando. Certifique-se de ter um ambiente de execução Java (JRE) instalado.

1.  **Navegue até o diretório:** Abra um terminal e navegue até a pasta onde os arquivos `.class` estão localizados.
2.  **Execute os testes:**
    * Para testar a referência de funcionários e o controle de bônus:
      ```bash
      java TestReference
      ```
    * Para testar a funcionalidade de um gerente:
      ```bash
      java TestManager
      ```
    * Para testar o sistema de autenticação:
      ```bash
      java TestSystem
      ```
    * Para testar um designer:
      ```bash
      java TestDesigner
      ```

### Demonstração

Os testes mostram como as diferentes classes interagem:

* **`TestReference`**: Demonstra o cálculo de bônus para diferentes tipos de funcionários (`Manager`, `Designer`, `VideoEditor`) e como o `BonusControl` adiciona esses bônus.
* **`TestManager`**: Cria um objeto `Manager` e um `Client`, define uma chave para o gerente e testa a autenticação.
* **`TestSystem`**: Cria instâncias de `Manager` e `Client`, configura uma chave para ambos e os autentica no `InternalSystem`.
* **`TestDesigner`**: Instancia um `Designer`, define seu nome, CPF e salário, e imprime seus dados e bônus.