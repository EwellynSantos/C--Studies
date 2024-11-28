# Switch

Usado para verificar múltiplos casos.

exemplo:

```csharp
int day = 3;

switch (day)
{
    case 1:
        Console.WriteLine("Domingo");
        break;
    case 2:
        Console.WriteLine("Segunda");
        break;
    case 3:
        Console.WriteLine("Terça");
        break;
    default:
        Console.WriteLine("Dia inválido");
        break;
}
```

* **`break`**: Finaliza a execução do caso atual.
* **`default`**: Executado quando nenhum caso corresponde.

