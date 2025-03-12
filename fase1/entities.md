# Entities

### 🔹 **O que são Entities?**

No contexto do **Entity Framework**, **entities** são classes C# que representam tabelas do banco de dados. Cada instância de uma entidade representa uma linha na tabela correspondente.

Elas geralmente possuem:\
✔ **Propriedades** que representam colunas do banco de dados.\
✔ **Chaves primárias** para identificação única de registros.\
✔ **Relacionamentos** com outras entidades.

### 🔹 **Exemplo de uma Entity em C#**

Imagine que temos uma tabela chamada `Customers` no banco de dados. Podemos representá-la com a seguinte classe em C#:

```csharp
csharpCopyEditpublic class Customer
{
    public int Id { get; set; }  // Chave primária
    public string Name { get; set; }
    public string Email { get; set; }
    public DateTime CreatedAt { get; set; } = DateTime.Now;
}
```

No Entity Framework, essa classe será mapeada automaticamente para uma tabela chamada `Customers` com as colunas `Id`, `Name`, `Email` e `CreatedAt`.
