# Tipos referencia

Os **tipos por referência** são aqueles que armazenam um **endereço de memória**, e não diretamente o valor. Isso significa que quando você passa um tipo por referência para uma variável ou método, está manipulando o **mesmo objeto na memória**. Se uma variável modificar o objeto, todas as outras variáveis que apontam para ele verão essa modificação.

Em **C#**, os principais tipos por referência incluem:

* `class` (classes)
* `interface`
* `delegate`
* `object`
* `string` (embora seja imutável)

#### 📌 Exemplo prático:

```csharp
using System;

class Pessoa
{
    public string Nome { get; set; }
}

class Program
{
    static void AlterarNome(Pessoa p)
    {
        p.Nome = "Novo Nome"; // Alteração afeta todas as referências desse objeto
    }

    static void Main()
    {
        Pessoa pessoa1 = new Pessoa { Nome = "Maria" };

        Console.WriteLine("Antes de chamar AlterarNome: " + pessoa1.Nome);

        AlterarNome(pessoa1);

        Console.WriteLine("Depois de chamar AlterarNome: " + pessoa1.Nome);
    }
}
```
