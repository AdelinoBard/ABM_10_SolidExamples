# Questão 01:

Em um sistema de gerenciamento de mídias sociais, a classe SocialMediaManager é responsável por gerenciar as postagens, comentários e interações nas redes sociais. No entanto, essa classe está crescendo rapidamente e possui métodos para interagir com todas as redes sociais disponíveis. Como podemos aplicar o Princípio da Segregação de Interface (ISP) a essa situação?

1. **Criar uma única interface `SocialMediaInterface` com todos os métodos relacionados às redes sociais.**

   - **Incorreto**
   - Esta abordagem viola o ISP porque a interface conteria métodos que algumas redes sociais podem não precisar. Por exemplo, uma rede social focada em imagens pode não precisar de métodos relacionados a postagens de texto extensas, tornando a interface pesada e forçando a implementação de métodos desnecessários.

2. **Adicionar todos os métodos relacionados às redes sociais na classe `SocialMediaManager`.**

   - **Incorreto**
   - Isso vai contra o ISP e também contra o Princípio da Responsabilidade Única (SRP). A classe `SocialMediaManager` se tornaria excessivamente grande e difícil de manter, além de estar fortemente acoplada a diversas redes sociais. Isso dificultaria futuras modificações e expansões.

3. **Dividir a classe `SocialMediaManager` em interfaces menores, como `PostManager`, `CommentManager` e `InteractionManager`.**

   - **Correto**
   - Esta é a maneira correta de aplicar o ISP. Cada interface separada define um conjunto específico de métodos que atendem a um propósito específico, permitindo que cada rede social implemente apenas os métodos relevantes para seu funcionamento. Isso torna o código mais modular e facilita a manutenção.

4. **Criar uma classe abstrata `SocialMediaBase` para centralizar todas as operações relacionadas às redes sociais.**

   - **Incorreto**
   - Embora a ideia de uma classe abstrata possa ser útil para compartilhar código comum, ela não necessariamente resolve o problema do ISP. Se a classe abstrata incluir métodos que nem todas as redes sociais usam, algumas subclasses serão forçadas a implementar métodos irrelevantes, violando o princípio.

5. **Deixar a classe `SocialMediaManager` como está, pois não é necessário aplicar o ISP a essa situação.**

   - **Incorreto**
   - Não aplicar o ISP pode resultar em uma classe altamente acoplada e difícil de expandir. A modularização com interfaces menores melhora a organização do código e sua capacidade de adaptação a diferentes redes sociais.

---

# Questão 02:

Em um sistema de comércio eletrônico, a classe `ProductManager` é responsável por gerenciar produtos, incluindo adicionar, remover, editar e exibir informações. Como podemos aplicar o Princípio da Segregação de Interface (ISP) a essa situação?

1. **Criar uma única interface `ProductInterface` com todos os métodos relacionados a produtos.**

   - **Incorreto**
   - Isso viola o ISP porque a interface se tornaria muito grande e conteria métodos que nem todas as classes precisam. Por exemplo, uma classe que apenas exibe produtos não deveria implementar métodos para adicionar ou editar produtos, tornando sua implementação confusa e desnecessária.

2. **Adicionar todos os métodos relacionados a produtos na classe `ProductManager`.**

   - **Incorreto**
   - Isso também viola o ISP e o Princípio da Responsabilidade Única (SRP). A classe `ProductManager` ficaria sobrecarregada, gerenciando todas as operações relacionadas a produtos. Isso dificultaria manutenção e testes, tornando o código menos modular.

3. **Criar uma classe abstrata `ProductBase` para centralizar todas as operações relacionadas a produtos.**

   - **Incorreto**
   - Embora uma classe abstrata possa ajudar a compartilhar código comum, ela não necessariamente resolve o problema do ISP. Se `ProductBase` contiver métodos que nem todas as subclasses precisam, algumas classes serão forçadas a implementar métodos irrelevantes, o que fere o princípio.

4. **Deixar a classe `ProductManager` como está, pois não é necessário aplicar o ISP a essa situação.**

   - **Incorreto**
   - O ISP é útil justamente para modularizar grandes classes e interfaces. Manter `ProductManager` com todos os métodos pode criar um código monolítico difícil de escalar. Separar responsabilidades torna o sistema mais flexível e de fácil manutenção.

5. **Dividir a classe `ProductManager` em interfaces menores, como `AddProductManager`, `EditProductManager`, `RemoveProductManager` e `DisplayProductManager`.**

   - **Correto**
   - Essa é a abordagem correta para aplicar o ISP. Criar interfaces menores permite que cada classe implemente apenas os métodos necessários, reduzindo dependências desnecessárias e facilitando a manutenção. Dessa forma, cada funcionalidade do sistema fica bem definida e separada.

---
