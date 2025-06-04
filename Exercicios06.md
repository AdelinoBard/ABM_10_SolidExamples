# Questão 01:

Em um sistema de gerenciamento de estoque, a classe `InventoryManager` depende diretamente da classe `DatabaseConnector` para acessar e atualizar os dados no banco de dados. Como podemos aplicar o Princípio da Inversão de Dependência (DIP) a essa situação?

1. **Manter a dependência direta entre `InventoryManager` e `DatabaseConnector`, pois isso simplifica o código.**

   - **Incorreto**
   - Manter uma dependência direta entre `InventoryManager` e `DatabaseConnector` viola o DIP, pois `InventoryManager` se torna fortemente acoplado a uma implementação específica de acesso ao banco de dados. Isso dificulta a manutenção e a testabilidade do código.

2. **Criar uma interface `DatabaseInterface` e fazer com que `InventoryManager` dependa da interface em vez da classe concreta `DatabaseConnector`.**

   - **Correto**
   - Esta é a abordagem correta para aplicar o DIP. Ao criar uma interface `DatabaseInterface`, `InventoryManager` pode depender dessa abstração, permitindo que diferentes implementações de acesso ao banco de dados sejam utilizadas sem modificar o código do gerenciador de estoque. Isso melhora a flexibilidade e a testabilidade do sistema.

3. **Adicionar métodos adicionais na classe `DatabaseConnector` para atender às necessidades específicas do `InventoryManager`.**

   - **Incorreto**
   - Adicionar métodos específicos do `InventoryManager` na classe `DatabaseConnector` viola o DIP, pois isso cria uma dependência direta e específica entre as duas classes. Isso torna o código menos modular e mais difícil de manter.

4. **Criar uma classe abstrata `DatabaseBase` para centralizar as operações relacionadas ao banco de dados.**

   - **Incorreto**
   - Embora uma classe abstrata possa ajudar a compartilhar código comum, ela não resolve o problema do DIP. Se `InventoryManager` depender de uma classe abstrata concreta, ainda haverá um acoplamento forte entre as classes, o que não é desejável.

5. **Utilizar diretamente consultas SQL na classe `InventoryManager` para acessar o banco de dados.**

   - **Incorreto**
   - Utilizar consultas SQL diretamente na classe `InventoryManager` viola o DIP e também o Princípio da Responsabilidade Única (SRP). Isso torna o código menos modular, mais difícil de testar e de manter, além de dificultar a reutilização do código em diferentes contextos.

---

# Questão 02:

Em um sistema de pagamento online, a classe `PaymentProcessor` é responsável por processar pagamentos e depende diretamente da classe `PaymentGateway` para se comunicar com o sistema de pagamento externo. Como podemos aplicar o Princípio da Inversão de Dependência (DIP) a essa situação?

1. **Manter a dependência direta entre `PaymentProcessor` e `PaymentGateway`, pois isso simplifica a integração com o sistema de pagamento.**

   - **Incorreto**
   - Manter uma dependência direta entre `PaymentProcessor` e `PaymentGateway` viola o DIP, pois `PaymentProcessor` se torna fortemente acoplado a uma implementação específica de gateway de pagamento. Isso dificulta a manutenção e a testabilidade do código, além de limitar a flexibilidade para trocar ou modificar o gateway de pagamento.

2. **Adicionar métodos adicionais na classe `PaymentGateway` para atender às necessidades específicas do `PaymentProcessor`.**

   - **Incorreto**
   - Adicionar métodos específicos do `PaymentProcessor` na classe `PaymentGateway` viola o DIP, pois isso cria uma dependência direta e específica entre as duas classes. Isso torna o código menos modular e mais difícil de manter, além de dificultar a reutilização do código.

3. **Criar uma interface `PaymentGatewayInterface` e fazer com que Paymen`tProcessor dependa da interface em vez da classe concreta `PaymentGateway`.**

   - **Correto**
   - Esta é a abordagem correta para aplicar o DIP. Ao criar uma interface `PaymentGatewayInterface`, `PaymentProcessor` pode depender dessa abstração, permitindo que diferentes implementações de gateways de pagamento sejam utilizadas sem modificar o código do processador de pagamentos. Isso melhora a flexibilidade e a testabilidade do sistema.

4. **Criar uma classe abstrata `PaymentBase` para centralizar as operações relacionadas a pagamentos.**

   - **Incorreto**
   - Embora uma classe abstrata possa ajudar a compartilhar código comum, ela não resolve o problema do DIP. Se `PaymentProcessor` depender de uma classe abstrata concreta, ainda haverá um acoplamento forte entre as classes, o que não é desejável.

5. **Utilizar diretamente chamadas HTTP na classe `PaymentProcessor` para se comunicar com o sistema de pagamento externo.**

   - **Incorreto**
   - Utilizar chamadas HTTP diretamente na classe `PaymentProcessor` viola o DIP e também o Princípio da Responsabilidade Única (SRP). Isso torna o código menos modular, mais difícil de testar e de manter, além de dificultar a reutilização do código em diferentes contextos.

---
