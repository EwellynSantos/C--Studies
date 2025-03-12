# Saída(Console)

Segue abaixo os exemplos de saida de dados pelo console:

#### 1️⃣ **Usando Concatenação de Strings (`+`)**

```csharp
int idade = 25;
string nome = "Alice";
Console.WriteLine("Nome: " + nome + ", Idade: " + idade);
```



#### 2️⃣ **Usando `string.Format()`**

```csharp
Console.WriteLine(string.Format("Nome: {0}, Idade: {1}", nome, idade));
```



#### 3️⃣ **Usando Interpolação de Strings (`$""`)** – **Recomendado** ✅✅

```csharp
Console.WriteLine($"Nome: {nome}, Idade: {idade}");
```



#### 4️⃣ **Usando `Console.WriteLine()` com múltiplos argumentos**

```csharp
Console.WriteLine("Nome: {0}, Idade: {1}", nome, idade);
```



#### 5️⃣ **Usando `Join` para Listas ou Arrays**

```csharp
csharpCopyEditstring[] dados = { nome, idade.ToString() };
Console.WriteLine(string.Join(", ", dados));
```
