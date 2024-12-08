# Entrada

para armazenar a entrada de valores pelo terminal podemos utilizar o ReadLine iu o Read, a diferença entre eles é que ao ReadLine só atribui o valor digitado após apertar o enter. sintaxe:

```csharp
Console.ReadLine()

ou 

Console.Read()
```

Exemplo:\


```csharp
using System;

namespace Calculator
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Clear();
            Console.WriteLine("Primeiro valor: ");
            //aqui le o valor e atribui a variavel valor1
            float valor1 = float.Parse(Console.ReadLine()); 

            Console.WriteLine(valor1);

        }
    }
}

```
