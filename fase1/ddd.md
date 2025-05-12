# DDD

🧠 Conceitos principais do DDD:\
Domínio\
\
É o contexto do problema real que o software tenta resolver (ex: sistema bancário, e-commerce, saúde).\
\
Modelagem do Domínio\
\
Envolve criar modelos conceituais com base no entendimento do domínio e da linguagem usada pelos especialistas (linguagem ubíqua).\
\
Linguagem Ubíqua (Ubiquitous Language)\
\
Um vocabulário comum e compartilhado entre equipe técnica e especialistas do negócio, refletido no código, documentação e conversas.\
\
Contexto Delimitado (Bounded Context)\
\
Define fronteiras claras onde um determinado modelo de domínio se aplica.\
\
Cada contexto tem sua linguagem própria, regras e modelos.\
\
Entidades\
\
Objetos com identidade única ao longo do tempo (ex: Cliente, Pedido).\
\
Mesmo que seus dados mudem, sua identidade persiste.\
\
Value Objects (Objetos de Valor)\
\
Objetos sem identidade própria, imutáveis, definidos apenas por seus atributos (ex: CPF, Endereço).\
\
Aggregates (Agregados)\
\
Um conjunto de entidades e objetos de valor com uma raiz (Aggregate Root) que controla o acesso e as regras de consistência.\
\
Repositórios\
\
Responsáveis por acessar e armazenar agregados, abstraindo a persistência de dados.\
\
Serviços de Domínio\
\
Representam ações do negócio que não pertencem a uma única entidade (ex: cálculo de juros, criação de fatura).\
\
📌 Vantagens do DDD:\
Foco no negócio real, e não apenas em tecnologia.\
\
Melhor comunicação com especialistas da área.\
\
Código mais expressivo e alinhado com o domínio.\
\
Facilita manutenção e evolução do sistema.\
\
Se quiser, posso montar um exemplo prático usando DDD em C#, com entidades, serviços e repositórios. Você quer isso?\
\
\
\
\
\
\
\
Is this conversation helpful so far?\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
ChatGPT can make mistakes. Check imp
