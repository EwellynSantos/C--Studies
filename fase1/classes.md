# Classes

Uma **classe** é um conjunto de atributos (variáveis) e métodos que definem o comportamento e o estado de um objeto. No C#, uma **classe** é um tipo de dado que serve como um molde para criar objetos. Ela encapsula dados (campos) e comportamento (métodos) em uma única unidade, promovendo a reutilização e organização do código. As classes são fundamentais na **Programação Orientada a Objetos (POO)**.



estrutura básica:

```csharp
class Pessoa
{
    // Atributos (campos)
    public string Nome;
    public int Idade;

    // Métodos
    public void Cumprimentar()
    {
        Console.WriteLine($"Olá, meu nome é {Nome} e tenho {Idade} anos.");
    }
}
```

### **Modificadores de Acesso**

Os membros de uma classe podem ter diferentes níveis de acesso para controlar a visibilidade:

<table><thead><tr><th width="230">Modificador</th><th>Descrição</th></tr></thead><tbody><tr><td><code>public</code></td><td>O membro pode ser acessado de qualquer lugar.</td></tr><tr><td><code>private</code></td><td>O membro só pode ser acessado dentro da própria classe.</td></tr><tr><td><code>protected</code></td><td>O membro pode ser acessado na própria classe e em classes derivadas.</td></tr><tr><td><code>internal</code></td><td>O membro pode ser acessado apenas dentro do mesmo assembly.</td></tr><tr><td><code>protected internal</code></td><td>Combinação de <code>protected</code> e <code>internal</code>.</td></tr><tr><td><code>private protected</code></td><td>Acesso limitado à própria classe e suas subclasses no mesmo assembly.</td></tr></tbody></table>



### **Construtores**

Um **construtor** é um método especial chamado automaticamente quando o objeto é criado. Ele é usado para inicializar os campos de uma classe.

#### **Construtor Padrão**

```csharp
class Pessoa
{
    public string Nome;
    public int Idade;

    public Pessoa() // Construtor
    {
        Nome = "Desconhecido";
        Idade = 0;
    }
}
```

### **Propriedades**

As **propriedades** fornecem uma maneira de acessar os campos de forma controlada, encapsulando a lógica de _get_ (obter) e _set_ (definir) valores.

#### **Propriedades Automáticas**

Uma versão mais simples:

```csharp
class Pessoa
{
    public string Nome { get; set; }
    public int Idade { get; set; }
}
```



### **Herança**

Uma classe pode herdar de outra usando o operador `:`. Isso permite reutilizar código e criar hierarquias.

```csharp
class Pessoa
{
    public string Nome;
    public void Saudacao()
    {
        Console.WriteLine($"Olá, meu nome é {Nome}.");
    }
}

class Estudante : Pessoa //herança
{
    public string Curso;

    public void MostrarCurso()
    {
        Console.WriteLine($"Eu estudo {Curso}.");
    }
}
```



### **Polimorfismo**

Permite que métodos em classes derivadas substituam métodos na classe base.

```csharp
class Animal
{
    public virtual void EmitirSom()
    {
        Console.WriteLine("Animal faz um som.");
    }
}

class Cachorro : Animal
{
    public override void EmitirSom()
    {
        Console.WriteLine("Cachorro late.");
    }
}

class Gato : Animal
{
    public override void EmitirSom()
    {
        Console.WriteLine("Gato mia.");
    }
}
```
