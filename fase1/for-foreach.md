# For / foreach



### for

Usado para repetir um bloco de código um número definido de vezes.

```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine($"Contagem: {i}");
}

```





### foreach

Itera por todos os elementos de uma coleção.

```csharp
string[] frutas = { "Maçã", "Banana", "Laranja" };

foreach (string fruta in frutas)
{
    Console.WriteLine(fruta);
}

```

