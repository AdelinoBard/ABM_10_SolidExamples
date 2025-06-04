# Questão 01:

Durante uma revisão de código, um desenvolvedor destaca a importância do Princípio de Substituição de Liskov (LSP) para a hierarquia de classes em um sistema. Qual é o principal objetivo do Princípio de Substituição de Liskov (LSP) na programação orientada a objetos:

1. **Permitir a substituição de métodos sem considerar o comportamento esperado.**

   - **Incorreto**
   - O LSP exige que classes derivadas mantenham o comportamento esperado da classe base. Se métodos forem substituídos sem considerar isso, podem surgir falhas inesperadas no sistema. O princípio garante que um objeto de uma subclasse possa ser utilizado no lugar da classe base sem efeitos colaterais indesejados.

2. **Garantir que cada classe tenha apenas uma responsabilidade bem definida.**

   - **Incorreto**
   - Embora a responsabilidade única seja uma boa prática de design (Princípio da Responsabilidade Única - SRP), o LSP não se concentra nisso. O LSP trata da substituição correta de classes derivadas sem comprometer o comportamento do sistema.

3. **Facilitar a modificação direta das classes existentes para adicionar novas funcionalidades.**

   - **Incorreto**
   - O LSP não se concentra na modificação direta de classes existentes. Em vez disso, ele assegura que subclasses possam ser usadas de forma intercambiável com suas classes base, mantendo o comportamento esperado. A modificação direta pode ser abordada por outros princípios, como o Aberto/Fechado (OCP).

4. **Limitar a capacidade de adicionar novas funcionalidades às classes existentes.**

   - **Incorreto**
   - O LSP não limita a adição de novas funcionalidades. Pelo contrário, ele permite que subclasses sejam estendidas com novas características, desde que mantenham o comportamento esperado da classe base. O objetivo é garantir que a hierarquia de classes permaneça coerente e previsível.

5. **Garantir que uma classe derivada possa substituir sua classe base sem alterar o comportamento esperado do programa.**

   - **Correto**
   - Este é o objetivo central do LSP! Ele assegura que uma subclasse possa ser usada no lugar da classe base sem alterar o comportamento esperado do programa. Isso evita problemas de compatibilidade e mantém a integridade do sistema, permitindo que subclasses sejam tratadas como instâncias da classe base.

---

# Questão 02:

Durante uma discussão sobre boas práticas de programação, um desenvolvedor destaca a importância do Princípio de Substituição de Liskov (LSP) para a coesão e flexibilidade do código. Por que é importante seguir o Princípio de Substituição de Liskov (LSP) ao projetar uma hierarquia de classes:

1. **Para permitir a substituição de métodos sem considerar o comportamento esperado.**

   - **Incorreto**
   - O LSP exige que subclasses mantenham o comportamento esperado da classe base. Se métodos forem substituídos sem essa consideração, o sistema pode apresentar falhas inesperadas, tornando o código menos confiável e difícil de manter.

2. **Para garantir que as classes derivadas possam ser substituídas por suas classes base sem alterar o comportamento esperado do programa.**

   - **Correto**
   - Este é exatamente o princípio do LSP! Ele garante que objetos de subclasses possam substituir objetos da classe base sem afetar a lógica do programa, preservando a integridade do sistema e permitindo flexibilidade no design.

3. **Para garantir que cada classe tenha apenas uma responsabilidade bem definida.**

   - **Incorreto**
   - A definição de uma única responsabilidade para cada classe está relacionada ao Princípio da Responsabilidade Única (SRP), não ao LSP. Embora ambos sejam importantes, o LSP se concentra na substituição correta de classes derivadas.

4. **Para facilitar a adição de novas funcionalidades às classes existentes.**

   - **Incorreto**
   - O LSP não trata diretamente da adição de funcionalidades. Em vez disso, ele ajuda a garantir que novas classes derivadas possam ser incorporadas sem causar problemas de compatibilidade. A extensão de funcionalidades é mais relacionada ao Princípio Aberto/Fechado (OCP).

5. **Para limitar a capacidade de extensão das funcionalidades das classes existentes.**

   - **Incorreto**
   - O LSP não limita a extensão de funcionalidades, mas sim define regras para que essa extensão seja feita corretamente, garantindo que subclasses não violem as expectativas da classe base.

---
