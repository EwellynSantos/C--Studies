# Condicional Ternária

#### ✅ **O que é a operação ternária?**

A operação ternária em C# é uma forma **concisa** de escrever uma **estrutura condicional** (como um `if/else`) em **uma única linha**.

***

#### 📌 **Sintaxe:**

```csharp
csharpCopyEditcondição ? valor_se_verdadeiro : valor_se_falso;
```

***

#### 🧠 **Como funciona?**

* Avalia a **condição**.
* Se for **true**, retorna `valor_se_verdadeiro`.
* Se for **false**, retorna `valor_se_falso`.

***

#### 💡 **Exemplo:**

```csharp
csharpCopyEditint idade = 18;
string resultado = idade >= 18 ? "Maior de idade" : "Menor de idade";
Console.WriteLine(resultado); // Saída: Maior de idade
```

***

#### 🧱 **Equivalente com if/else:**

```csharp
csharpCopyEditstring resultado;
if (idade >= 18)
    resultado = "Maior de idade";
else
    resultado = "Menor de idade";
```
