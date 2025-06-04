# Questão 01:

Considere uma aplicação de processamento de pagamentos que usa a classe PaymentProcessor para processar diferentes tipos de pagamentos. Inicialmente, a aplicação suporta apenas pagamentos com cartão de crédito. Agora, há uma demanda para adicionar suporte para pagamentos via PayPal sem modificar o código existente da classe PaymentProcessor. Qual das alternativas abaixo representa a melhor abordagem para seguir o Princípio Aberto-Fechado (OCP):

1. **Modificar a classe `PaymentProcessor` para incluir um método `processPayPalPayment`**

   - **Incorreto**
   - Isso **viola o OCP** porque exige modificar a classe existente, o que pode introduzir problemas e exigir testes adicionais. Toda vez que um novo método de pagamento for adicionado, a classe precisará ser alterada novamente.

2. **Criar uma nova classe `PayPalPaymentProcessor` que herda de `PaymentProcessor` e adiciona o método `processPayPalPayment`**

   - **Incorreto**
   - Embora pareça uma abordagem modular, **não é a melhor solução**, pois uma subclasse estaria sendo criada apenas para adicionar um comportamento específico. Isso pode levar a um modelo rígido e um acoplamento indesejado.

3. **Adicionar um `if` na classe `PaymentProcessor` para verificar o tipo de pagamento e chamar o método apropriado**

   - **Incorreto**
   - Isso também **viola o OCP**, pois exige modificar a classe `PaymentProcessor` toda vez que um novo tipo de pagamento for adicionado, resultando em código mais complexo e menos flexível.

4. **Modificar a classe `PaymentProcessor` para suportar ambos os tipos de pagamento através de métodos sobrecarregados**

   - **Incorreto**
   - Embora a sobrecarga possa ser útil em alguns contextos, **ainda exige modificações diretas na classe `PaymentProcessor`**, o que a torna uma abordagem incorreta segundo o OCP.

5. **Utilizar uma interface `PaymentMethod` e fazer com que `PaymentProcessor` dependa dessa interface ao invés de classes concretas**

   - **Correto**
   - **Essa é a melhor abordagem!** Criar uma interface `PaymentMethod` permite que novos tipos de pagamento sejam adicionados sem modificar `PaymentProcessor`. Cada novo método de pagamento pode implementar essa interface e ser utilizado sem impactar o código existente.

---

# Questão 02:

Imagine que você está desenvolvendo um sistema de notificações que envia mensagens através de diferentes canais (e-mail, SMS, push notifications). A classe `NotificationService` foi originalmente projetada para enviar apenas e-mails. Como você pode refatorar o sistema para adicionar novos canais de notificação (SMS, push notifications) sem violar o Princípio Aberto-Fechado (OCP):

1. **Modificar a classe `NotificationService` para incluir métodos para cada tipo de notificação (`sendEmail`, `sendSMS`, `sendPushNotification`).**

   - **Incorreto**
   - Aqui, toda vez que adicionamos um novo canal, precisamos modificar `NotificationService`, quebrando o princípio. Isso causa problemas de manutenção e aumenta o acoplamento.

2. **Adicionar um parâmetro ao método `sendNotification` em `NotificationService` para indicar o tipo de notificação.**

   - **Incorreto**
   - Essa abordagem exigiria um grande bloco de `if-else` ou `switch`, tornando o código difícil de manter. Se quisermos adicionar um novo tipo de notificação, precisaríamos modificar `NotificationService` diretamente.

3. **Criar subclasses de `NotificationService` para cada tipo de notificação (`EmailNotificationService`, `SMSNotificationService`, `PushNotificationService`)**.

   - **Incorreto**
   - Embora pareça uma solução modular, isso viola o OCP porque exige a criação de **novas subclasses** sempre que um novo canal for adicionado. Além disso, a responsabilidade de envio de notificações deveria estar **nos canais de comunicação**, e não diretamente em `NotificationService`.

4. **Usar um padrão Singleton para cada tipo de notificação dentro da classe `NotificationService`.**

   - **Incorreto**
   - O padrão Singleton não é necessário aqui e pode complicar a estrutura sem necessidade. Ele resolveria a questão da instância única, mas não ajudaria a tornar o código extensível sem modificação.

5. **Definir uma interface `NotificationChannel` com um método `sendNotification` e criar implementações concretas para e-mail, SMS e push notifications.**

   - **Correto**
   - Essa abordagem segue o OCP perfeitamente. Criamos uma interface `NotificationChannel` e implementamos classes concretas (`EmailNotification`, `SMSNotification`, `PushNotification`).
   - Se quisermos adicionar um novo tipo de notificação no futuro, basta criar uma nova classe que implementa `NotificationChannel`, sem alterar `NotificationService`.

---

## Exemplo de código:

```csharp
using System;

interface INotificationChannel
{
    void SendNotification(string message);
}

class EmailNotification : INotificationChannel
{
    public void SendNotification(string message)
    {
        Console.WriteLine("Enviando e-mail: " + message);
    }
}

class SMSNotification : INotificationChannel
{
    public void SendNotification(string message)
    {
        Console.WriteLine("Enviando SMS: " + message);
    }
}

class PushNotification : INotificationChannel
{
    public void SendNotification(string message)
    {
        Console.WriteLine("Enviando Push Notification: " + message);
    }
}

class NotificationService
{
    private readonly INotificationChannel _channel;

    public NotificationService(INotificationChannel channel)
    {
        _channel = channel;
    }

    public void Send(string message)
    {
        _channel.SendNotification(message);
    }
}

class Program
{
    static void Main()
    {
        // Testando envio de notificações
        NotificationService emailService = new NotificationService(new EmailNotification());
        emailService.Send("Olá, este é um e-mail!");

        NotificationService smsService = new NotificationService(new SMSNotification());
        smsService.Send("Mensagem via SMS!");

        NotificationService pushService = new NotificationService(new PushNotification());
        pushService.Send("Push Notification enviada!");
    }
}
```

---
