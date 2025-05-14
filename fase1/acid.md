# ACID

ACID são propriedades de transaçoes de um banco de dados

A - Atomicidade

C - Consistência

I - Isolamento

D - Durabilidade



### Atomicidade

Garante transaçoes atômicas. E o que seroa? basicamente é iniciada uma trasação, onde precisa garantir que todos os passis dessa transação esteja ok, e se não houver problemas, ao final da transação faremos um commit. Caso haja um erro no meio dessa transação, é feito um rollback e as alteraçoes não são realizadas/commitadas.



### Consistência

Precisamos garantir que os dados sigam as regras do banco. Ou seja, os dados precisam estar corretos de acordo com seus tipos. Além de chaves estrangeiras, primarias e também restrições(NOT NULL, Cascade, Unique)



### Isolamento

Nesse caso enquanto realizamos uma transação(insert, delete e etc) de um dado especifico, se houver outra transação para o mesmo dado, a primeira transação é isolada, e a segunda transação só pode ser iniciada a partir que a primeira finalize.



### Durabilidade

Os dados, uma vez persistidos, devem continuar armazenados. O que significa, que antes de uma transação terminar, os dados precisam ser registrados em uma memória não volátil (disco, HD, SSD)



Outra explicação:\
\
**O que é ACID?**

**ACID** é um conjunto de propriedades que garante que as **transações em um banco de dados** sejam executadas de forma **confiável, consistente e segura**.

***

### 🔍 Significado da sigla:

<table><thead><tr><th width="59">Letra</th><th width="235">Nome</th><th>O que significa</th></tr></thead><tbody><tr><td><strong>A</strong></td><td><strong>Atomicidade (Atomicity)</strong></td><td>A transação é <strong>tudo ou nada</strong>: ou todas as operações são concluídas com sucesso, ou nenhuma é aplicada.</td></tr><tr><td><strong>C</strong></td><td><strong>Consistência (Consistency)</strong></td><td>A transação leva o banco de um estado <strong>válido a outro estado válido</strong>, mantendo as <strong>regras de integridade</strong> dos dados.</td></tr><tr><td><strong>I</strong></td><td><strong>Isolamento (Isolation)</strong></td><td>Transações simultâneas não interferem entre si. Os efeitos de uma transação <strong>não são visíveis para outras</strong> até que ela termine.</td></tr><tr><td><strong>D</strong></td><td><strong>Durabilidade (Durability)</strong></td><td>Uma vez que a transação é confirmada (<strong>commit</strong>), seus efeitos <strong>permanecem</strong>, mesmo em caso de falha de energia ou sistema.</td></tr></tbody></table>

