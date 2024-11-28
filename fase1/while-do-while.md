# While / do-while



### While

Executa o bloco enquanto a condição for verdadeira.

```csharp
int x = 0;
while (x < 3)
{
    Console.WriteLine($"x: {x}");
    x++;
}

```





### do-while

Executa o bloco ao menos uma vez, mesmo que a condição seja falsa.

```csharp
int x = 5;
do
{
    Console.WriteLine($"x: {x}");
    x++;
} while (x < 3);
```
