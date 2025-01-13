# Modificadores de acesso

Os **modificadores de acesso** em C# controlam a visibilidade e o alcance de classes, métodos, propriedades e outros membros. Eles são fundamentais para implementar o **encapsulamento**, permitindo que você defina claramente quais partes do seu código podem ser acessadas ou modificadas por outras partes.

***

### **1. Tipos de Modificadores de Acesso**

#### **1.1 `public`**

* Torna o membro acessível de qualquer lugar no programa.
* É o modificador mais permissivo.
* Comumente usado para expor APIs ou métodos públicos de uma classe.

**Exemplo:**

```csharp
public class MinhaClasse
{
    public string Nome { get; set; } // Acessível de qualquer lugar
}
```

***

#### **1.2 `private`**

* Restringe o acesso ao membro apenas dentro da mesma classe.
* É o mais restritivo.
* Usado para proteger dados ou comportamentos que não devem ser expostos diretamente.

**Exemplo:**

```csharp
public class MinhaClasse
{
    private string senha; // Apenas a classe MinhaClasse pode acessar isso

    public void DefinirSenha(string novaSenha)
    {
        senha = novaSenha;
    }
}
```

***

#### **1.3 `protected`**

* Permite que o membro seja acessado na mesma classe ou em classes derivadas.
* Útil em cenários de herança.

**Exemplo:**

```csharp
public class Base
{
    protected int Numero { get; set; }
}

public class Derivada : Base
{
    public void MostrarNumero()
    {
        Console.WriteLine($"Número: {Numero}");
    }
}
```

***

#### **1.4 `internal`**

* Torna o membro acessível dentro do mesmo assembly (projeto).
* Ideal para manter os membros acessíveis apenas dentro do projeto, mas não para consumidores externos.

**Exemplo:**

```csharp
internal class MinhaClasseInterna
{
    internal string Mensagem { get; set; }
}
```

***

#### **1.5 `protected internal`**

* Combina os modificadores `protected` e `internal`.
* O membro pode ser acessado por:
  * Classes no mesmo assembly.
  * Classes derivadas, mesmo que estejam em assemblies diferentes.

**Exemplo:**

```csharp
public class Base
{
    protected internal string Mensagem { get; set; }
}

public class Derivada : Base
{
    public void MostrarMensagem()
    {
        Console.WriteLine(Mensagem);
    }
}
```

***

#### **1.6 `private protected`**

* Introduzido no C# 7.2.
* Permite que o membro seja acessado por:
  * Classes derivadas **dentro do mesmo assembly**.
* É uma combinação mais restritiva de `private` e `protected`.

**Exemplo:**

```csharp
public class Base
{
    private protected string Mensagem { get; set; }
}

public class Derivada : Base
{
    public void MostrarMensagem()
    {
        Console.WriteLine(Mensagem);
    }
}
```





### Comparação entre modificadores

<figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

### **Boas Práticas**

* Use `private` sempre que possível para proteger dados sensíveis.
* Use `public` para expor APIs ou funcionalidades que outras classes precisarão acessar.
* Use `protected` em cenários de herança quando as classes derivadas precisarem acessar membros específicos.
* Use `internal` para limitar o escopo de membros ao mesmo assembly.
* Evite usar `protected internal` ou `private protected` a menos que seja realmente necessário.
