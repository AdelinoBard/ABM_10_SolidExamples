# Questão 01:

Durante uma sessão de revisão de código, um desenvolvedor explica a importância do Princípio de Responsabilidade Única (SRP) para a qualidade do software. Qual é o principal benefício de seguir o Princípio de Responsabilidade Única (SRP) ao projetar classes em um sistema:

1. **"Aumenta a complexidade do código, tornando-o mais desafiador de entender."**

   - **Incorreto**
   - O SRP busca reduzir a complexidade do código, garantindo que cada classe tenha **uma única responsabilidade**. Isso facilita a leitura e manutenção do código, pois cada classe tem um propósito claro e bem definido.

2. **"Facilita a reutilização de código em diferentes partes do sistema."**

   - **Incorreto**
   - Embora o SRP **possa** contribuir indiretamente para a reutilização do código, **esse não é o seu principal benefício**. O foco do princípio está em evitar que uma única classe tenha múltiplas responsabilidades, tornando o código **mais modular e fácil de modificar**.

3. **"Promove uma estrutura mais modular, facilitando a adição de novas funcionalidades."**

   - **Correto**
   - Quando aplicamos o SRP, criamos classes que seguem um propósito bem definido. Isso **torna o sistema mais modular**, facilitando a inclusão de novas funcionalidades sem comprometer outras partes do código. Além disso, mudanças em uma classe não impactam desnecessariamente outras classes.

4. **"Permite que uma classe tenha várias responsabilidades, simplificando o código."**

   - **Incorreto**
   - O SRP **proíbe** que uma classe tenha múltiplas responsabilidades. O objetivo é justamente o contrário: **evitar** que uma única classe lide com diversas funções, pois isso torna o código **difícil de manter e entender**.

5. **"Reduz a necessidade de documentação do código, pois cada classe é autoexplicativa."**

   - **Incorreto**
   - Embora o SRP possa tornar o código **mais intuitivo**, isso **não elimina** a necessidade de documentação. A documentação continua sendo essencial para explicar a lógica do sistema, como as classes interagem e como os princípios foram aplicados.

---

# Questão 02:

Durante uma discussão sobre boas práticas de programação, um desenvolvedor menciona a importância do SRP para o design de software. Por que é importante que cada classe siga o Princípio de Responsabilidade Única (SRP):

1. **"Para facilitar a manutenção do código ao ter responsabilidades bem definidas."**

   - **Correto**
   - O SRP afirma que cada classe deve ter **apenas uma razão para mudar**, ou seja, deve ter **uma única responsabilidade**.
   - Isso facilita a manutenção, pois qualquer modificação afeta apenas um aspecto específico da classe, sem impactar outras funcionalidades.

2. **"Para aumentar a complexidade do código e torná-lo mais desafiador de entender."**

   - **Incorreto**
   - O objetivo do SRP é **reduzir** a complexidade, não aumentá-la.
   - Quando cada classe tem um papel bem definido, o código se torna **mais organizado, legível e fácil de entender**.

3. **"Para permitir que uma classe tenha várias responsabilidades e simplifique o código."**

   - **Incorreto**
   - O SRP **proíbe** que uma classe tenha múltiplas responsabilidades.
   - Ao concentrar várias funções em uma única classe, o código **fica mais difícil de manter e testar**, pois mudanças podem afetar várias partes inesperadamente.

4. **"Para reduzir a modularidade do código e evitar a adição de novas funcionalidades."**

   - **Incorreto**
   - O SRP **aumenta** a modularidade, permitindo que novas funcionalidades sejam adicionadas sem interferir no código existente.
   - Classes bem separadas e independentes tornam o sistema mais **flexível e expansível**.

5. **"Para impor um controle estrito sobre o acesso aos métodos das classes."**

   - **Incorreto**
   - O controle de acesso aos métodos é uma preocupação mais ligada à **encapsulamento**, não diretamente ao SRP.
   - O princípio foca em **separação de responsabilidades**, e não em como os métodos são acessados dentro de uma classe.

---
