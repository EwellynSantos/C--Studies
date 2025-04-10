# Params

#### 🔹 O que é `params`?

O modificador `params` permite que um método receba um **número variável de argumentos** como um array. Ele é usado quando **não se sabe quantos parâmetros serão passados** para o método.

***

#### 🔹 Como usar?

A sintaxe básica é:

```csharp
csharpCopyEditpublic void Exemplo(params int[] numeros)
{
    foreach (var numero in numeros)
    {
        Console.WriteLine(numero);
    }
}
```

Esse método pode ser chamado de várias formas:

```csharp
csharpCopyEditExemplo(1, 2, 3);           // três argumentos
Exemplo();                  // nenhum argumento
Exemplo(new int[] { 4, 5 }); // array como argumento
```

***

#### 🔹 Regras importantes:

* Só pode haver **um parâmetro `params`** por método.
* Ele deve ser o **último parâmetro** da lista de parâmetros.
* Pode ser usado com **qualquer tipo de array** (ex: `params string[]`, `params object[]`).

***

#### 🔹 Quando usar?

* Quando você quer permitir **flexibilidade** no número de argumentos.
* Para criar **métodos mais reutilizáveis**, como somar valores, construir mensagens, etc.
