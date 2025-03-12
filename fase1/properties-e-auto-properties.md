# Properties e auto properties



### Properties

São definiçoes de métodos encapsulados, porém expondo uma sintaxe similar a de atributos e nãp de métodos.

<figure><img src=".gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

<mark style="color:orange;">Exemplo:</mark>

```csharp
public class Pessoa{

// Propriedade comum com lógica personalizada no setter
public string Nome
    {
        get { return _nome; }
        set
        {
            if (!string.IsNullOrWhiteSpace(value))
                _nome = value;
            else
                throw new ArgumentException("Nome não pode ser vazio.");
        }
    }
}

```





### Auto properties

é uma forma simplificada de se declarar propriedades que nao necessitam lógicas particulares para as opererações get e set

Exemplo:

```csharp
public class Pessoa{

     // Auto-property (o C# gera automaticamente o campo privado)
    public int Idade { get; set; }

    // Auto-property somente leitura (somente pode ser definida no construtor)
    public string Nacionalidade { get; } = "Brasileira";
}
```
