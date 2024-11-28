# Métodos

Métodos armazenam diversas instruções para  serem executadas quando chamado. Além disso,  sempre devemos iniciar o método com o tipo de retorno.&#x20;

Um **método** é uma função definida dentro de uma classe que realiza uma ação específica.

Sintaxe:

```csharp
[Modificador] [Tipo de Retorno] NomeDoMetodo([Parâmetros])
{
    // Corpo do método
    return valor; // Opcional, dependendo do tipo de retorno
}

```

ex:

```csharp
public int Somar(int a, int b)
{
    return a + b;
}

```

### Tipos de Métodos

* **Métodos com retorno**: Retornam um valor.
* **Métodos sem retorno (`void`)**: Não retornam nada, apenas executam uma ação.

Exemplo com Retorno

```csharp
public double CalcularArea(double largura, double altura)
{
    return largura * altura;
}

```

Exemplo Sem Retorno

```csharp
public void ExibirMensagem(string mensagem)
{
    Console.WriteLine(mensagem);
}
```



<table><thead><tr><th>Tipo</th><th width="393">Descrição</th></tr></thead><tbody><tr><td>void</td><td>é um retorno vazio</td></tr><tr><td></td><td></td></tr><tr><td></td><td></td></tr></tbody></table>
