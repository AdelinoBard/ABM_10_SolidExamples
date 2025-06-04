# Questão 01:

Durante uma reunião de equipe, um desenvolvedor júnior está aprendendo sobre os Princípios SOLID com seus colegas mais experientes. Qual é o objetivo principal do Princípio da Responsabilidade Única (SRP) na programação de software:

1. **"Permitir que uma classe tenha várias responsabilidades para simplificar o código."**

   - **Incorreto**
   - O Princípio da Responsabilidade Única (SRP) defende que cada classe deve ter **apenas uma responsabilidade bem definida**. Se uma classe assume múltiplas responsabilidades, isso aumenta a complexidade do código e torna mais difícil sua manutenção e teste.

2. **"Aumentar a complexidade do código para torná-lo mais desafiador."**

   - **Incorreto**
   - O objetivo do SRP não é tornar o código mais difícil, mas sim torná-lo mais **fácil de entender e manter**. A separação de responsabilidades reduz dependências entre componentes do sistema e facilita futuras modificações.

3. **"Reduzir a modularidade do código para facilitar sua manutenção."**

   - **Incorreto**
   - O SRP **favorece a modularidade**, pois quando cada classe tem uma única responsabilidade, o código fica mais organizado e modular, permitindo alterações sem afetar outras partes do sistema.

4. **"Impor um controle estrito sobre o acesso aos métodos das classes."**

   - **Incorreto**
   - O SRP **não trata especificamente do controle de acesso aos métodos**. Embora a encapsulação seja importante, o foco do SRP é garantir que cada classe **tenha apenas uma responsabilidade**, evitando que uma classe lide com múltiplas funções ao mesmo tempo.

5. **"Garantir que cada classe tenha apenas uma responsabilidade bem definida."**

   - **Correto**
   - Este é **o princípio central do SRP**. A ideia é que cada classe **deve ter um único motivo para mudar**, ou seja, uma única responsabilidade bem definida. Isso melhora a organização do código, facilita a reutilização e torna o sistema mais robusto.

---

# Questão 02:

Durante uma sessão de revisão de código, um desenvolvedor destaca a importância do Princípio de Substituição de Liskov (LSP) para a hierarquia de classes. Qual é o objetivo principal do Princípio de Substituição de Liskov (LSP) na programação de software:

1. **Restringir a herança entre as classes para evitar complexidade**

   - **Incorreto**
   - O LSP **não restringe** a herança. Ele garante que uma subclasse pode ser usada no lugar da classe base sem causar problemas inesperados. O princípio visa **preservar a compatibilidade** e evitar violações da lógica do sistema. Restringir herança arbitrariamente pode ser prejudicial ao design do software.

2. **Permitir a substituição de métodos sem considerar o comportamento esperado**

   - **Incorreto**
   - Isso **vai contra** o LSP. O princípio determina que, ao substituir ou estender uma classe, **o comportamento esperado deve ser mantido**. Se um método é substituído e altera o comportamento da classe de forma inesperada, pode causar **erros no sistema**.

3. **Limitar a capacidade de adicionar novas funcionalidades às classes existentes**

   - **Incorreto**
   - O LSP **não limita a adição de funcionalidades**, mas impõe que, ao adicionar novas características, o comportamento das subclasses **deve continuar coerente com a classe base**. O objetivo é permitir a expansão do sistema sem comprometer a previsibilidade do código.

4. **Tornar o código mais difícil de entender ao introduzir múltiplas camadas de herança**

   - **Incorreto**
   - O LSP **não tem relação direta** com tornar o código mais difícil de entender. Pelo contrário, ao **garantir substituições seguras**, ele melhora a manutenção e previsibilidade do código. A complexidade do sistema depende de vários fatores, como **má implementação** de princípios de design.

5. **Permitir que uma classe seja estendida por outras classes, mantendo a coerência do comportamento**

   - **Correto**
   - O objetivo principal do LSP é **assegurar que subclasses possam substituir suas classes base sem alterar o comportamento do sistema**. Isso permite uma **herança segura** e evita que mudanças em uma subclasse causem problemas inesperados no restante do código.
   - O Princípio de Substituição de Liskov é fundamental para manter um código **flexível e sustentável**, garantindo que qualquer classe derivada possa ser usada de forma intercambiável com sua classe pai sem efeitos colaterais indesejados.

---
