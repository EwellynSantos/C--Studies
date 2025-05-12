# Mensageria

📬 O que é Mensageria?\
Mensageria é um modelo de comunicação entre sistemas ou serviços através do envio e recebimento de mensagens assíncronas, geralmente por meio de brokers (intermediários) como RabbitMQ, Apache Kafka, Azure Service Bus, entre outros.\
\
Ela é muito usada em arquiteturas de microsserviços para desacoplar serviços e permitir comunicação resiliente, escalável e tolerante a falhas.\
\
🧠 Conceitos principais:\
Conceito	Descrição\
Produtor (Publisher)	Envia (publica) uma mensagem para o broker.\
Consumidor (Consumer)	Recebe (consome) a mensagem do broker.\
Broker de Mensagens	Software intermediário que recebe, armazena e distribui mensagens (ex: RabbitMQ, Kafka).\
Fila (Queue)	Armazena mensagens até que sejam processadas (FIFO).\
Tópico (Topic)	Permite publicação para múltiplos assinantes (pub/sub).\
Mensagem	Estrutura de dados enviada entre os serviços, geralmente em JSON, XML, Protobuf etc.\
\
✅ Vantagens da Mensageria:\
Comunicação assíncrona (não bloqueante)\
\
Desacoplamento entre os serviços\
\
Suporte a retries, dead-letter queues, e garantia de entrega\
\
Escalabilidade (múltiplos consumidores processando em paralelo)\
\
Ideal para eventos de domínio (ex: OrderCreated, PaymentProcessed)\
\
🔧 Exemplos de ferramentas de mensageria:\
Ferramenta	Tipo	Destaque\
RabbitMQ	Fila (fila + troca de mensagens - AMQP)	Fácil de usar, muito usado com .NET\
Apache Kafka	Streaming baseado em logs	Alta performance, ideal para big data e eventos\
Azure Service Bus	Mensageria na nuvem	Nativo no ecossistema Azure\
Amazon SQS/SNS	Fila e pub/sub gerenciado	Escalável, simples, usado com AWS\
\
💡 Mensageria no .NET / C#\
🧰 Bibliotecas populares:\
MassTransit: abstração de mensageria para RabbitMQ, Azure Service Bus, Kafka, etc.\
\
EasyNetQ: biblioteca simples para RabbitMQ.\
\
Confluent.Kafka: cliente oficial do Apache Kafka para .NET.\
\
Azure.Messaging.ServiceBus: biblioteca da Microsoft para Azure Service Bus.
