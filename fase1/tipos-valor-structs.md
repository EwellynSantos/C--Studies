# Tipos valor (structs)

Os **tipos por valor** armazenam os **dados diretamente na memória**. Isso significa que quando você atribui um tipo por valor a outra variável, está criando **uma cópia independente** do valor original. Alterações em uma cópia **não afetam o valor original**.

Em **C#**, os tipos por valor incluem:

* Tipos numéricos (`int`, `double`, `float`, `decimal`, `byte`, etc.)
* Tipos booleanos (`bool`)
* `char`
* `struct`
* `enum`



### 📌 Exemplo prático:

```csharp
csharpCopyEditusing System;

class Program
{
    static void Dobrar(int numero)
    {
        numero = numero * 2; // Isso não altera o valor original
    }

    static void Main()
    {
        int valor = 10;

        Console.WriteLine("Antes de chamar Dobrar: " + valor);

        Dobrar(valor);

        Console.WriteLine("Depois de chamar Dobrar: " + valor); // Continua 10
    }
}
```

***

### 🎯 Ex
