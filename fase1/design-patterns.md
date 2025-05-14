# Design Patterns

### 🎨 O que são **Design Patterns**?

**Design Patterns** (ou **Padrões de Projeto**) são **soluções reutilizáveis para problemas comuns de design de software**.\
Eles **não são código pronto**, mas **modelos ou estratégias** que ajudam a escrever código mais **flexível, reutilizável e de fácil manutenção**.

***

#### 📚 Origem

Popularizados pelo livro "**Design Patterns: Elements of Reusable Object-Oriented Software**" (1994), dos autores conhecidos como _Gang of Four (GoF)_.

***

### 🔍 Por que usar?

* Evita reinventar a roda
* Melhora a clareza do código
* Facilita a manutenção e evolução
* Promove boas práticas de orientação a objetos
* Ajuda na comunicação entre desenvolvedores (vocabulário comum)

***

### 🧱 Classificação dos Design Patterns

#### 1. **Padrões Criacionais**

👉 Focados na **criação de objetos** de forma flexível.

| Padrão               | Função                                                  |
| -------------------- | ------------------------------------------------------- |
| **Singleton**        | Garante uma única instância de uma classe               |
| **Factory Method**   | Cria objetos via método, delegando a lógica à subclasse |
| **Abstract Factory** | Cria famílias de objetos relacionados                   |
| **Builder**          | Cria objetos complexos passo a passo                    |
| **Prototype**        | Clona objetos existentes                                |

***

#### 2. **Padrões Estruturais**

👉 Lidam com a **composição e estrutura de classes e objetos**.

| Padrão        | Função                                                      |
| ------------- | ----------------------------------------------------------- |
| **Adapter**   | Converte a interface de uma classe em outra esperada        |
| **Bridge**    | Separa abstração da implementação                           |
| **Composite** | Trata objetos individuais e compostos da mesma forma        |
| **Decorator** | Adiciona responsabilidades a um objeto dinamicamente        |
| **Facade**    | Fornece uma interface simplificada para um sistema complexo |
| **Flyweight** | Compartilha objetos comuns para economizar memória          |
| **Proxy**     | Substitui um objeto real por um representante               |

***

#### 3. **Padrões Comportamentais**

👉 Focados na **comunicação entre objetos e responsabilidades**.

| Padrão                      | Função                                                          |
| --------------------------- | --------------------------------------------------------------- |
| **Observer**                | Permite que objetos reajam a mudanças em outro objeto (pub/sub) |
| **Strategy**                | Permite trocar algoritmos em tempo de execução                  |
| **Command**                 | Encapsula comandos como objetos                                 |
| **Chain of Responsibility** | Encadeia objetos para tratar uma solicitação                    |
| **State**                   | Altera o comportamento do objeto conforme seu estado            |
| **Template Method**         | Define um esqueleto de algoritmo em uma classe base             |
| **Mediator**                | Centraliza a comunicação entre objetos                          |
| **Memento**                 | Permite salvar e restaurar o estado de um objeto                |
| **Visitor**                 | Permite adicionar novas operações a estruturas de objetos       |
