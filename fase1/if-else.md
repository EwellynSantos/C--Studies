# If/else



### if

Executa um bloco de código se uma condição for verdadeira.

```csharp
int x = 10;

if (x > 5)
{
    Console.WriteLine("x é maior que 5");
}
```





### if-else

Define um bloco alternativo caso a condição seja falsa.

```csharp
int x = 3;
if (x > 5)
{
    Console.WriteLine("x é maior que 5");
}
else
{
    Console.WriteLine("x é menor ou igual a 5");
}

```





### else if

Permite testar várias condições.

```csharp
int x = 5;
if (x > 10)
{
    Console.WriteLine("Maior que 10");
}
else if (x == 5)
{
    Console.WriteLine("Igual a 5");
}
else
{
    Console.WriteLine("Menor que 10 e diferente de 5");
}

```



