# Nullable

### 🔹 **Nullable em C#**

O conceito de **Nullable** (nulo) permite que **tipos de valor** (`int`, `bool`, `double`, etc.) possam armazenar `null`, algo que normalmente só é permitido para **tipos de referência** (`string`, `object`, `class`, etc.).

***

#### 1️⃣ **Nullable para Tipos de Valor (`int?`, `bool?`, etc.)**

Por padrão, tipos de valor **não podem** ser `null`.\
Para permitir `null`, usamos **`?`**:

```csharp
csharpCopyEditint? idade = null; // Correto
bool? ativo = null; // Correto
```

*   **Acessando o valor com `.Value`**:

    ```csharp
    csharpCopyEditint? numero = 10;
    Console.WriteLine(numero.Value); // 10
    ```
*   **Verificando se tem valor com `.HasValue`**:

    ```csharp
    csharpCopyEditif (idade.HasValue)
        Console.WriteLine("Idade: " + idade.Value);
    else
        Console.WriteLine("Idade não informada");
    ```

***

#### 2️⃣ **Operador de Coalescência Nula (`??`)**

Se uma variável nullable for `null`, podemos definir um valor padrão com `??`:

```csharp
csharpCopyEditint? numero = null;
int resultado = numero ?? 0; // Se for null, assume 0
Console.WriteLine(resultado); // 0
```

***

#### 3️⃣ **Nullable Reference Types (C# 8+)**

Desde o C# 8, é possível ativar **Nullable Reference Types**, onde o compilador avisa se um objeto pode ser `null`, ajudando a evitar exceções **`NullReferenceException`**.

*   **Ativando no projeto (`.csproj`)**:

    ```xml
    xmlCopyEdit<Nullable>enable</Nullable>
    ```
*   **Exemplo**:

    ```csharp
    csharpCopyEditstring? nome = null; // O compilador avisa que pode ser null
    ```
*   **Forçando um valor com `!` (null-forgiving operator)**:

    ```csharp
    csharpCopyEditstring? texto = null;
    Console.WriteLine(texto!.Length); // Assumimos que nunca será null (Cuidado!)
    ```

***

### ✅ **Resumindo**

✔ **`int?`, `bool?`, etc., permitem `null` para tipos de valor**.\
✔ **Operador `??` define valores padrão para `null`**.\
✔ **C# 8+ permite nullable em tipos de referência (`string?`)**.\
✔ **Use `.HasValue`, `.Value` e `??` para evitar exceções**.

Precisa de mais detalhes? 😊
