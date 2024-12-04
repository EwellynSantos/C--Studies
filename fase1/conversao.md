# Conversão

### Conversão entre tipos

C# permite conversões de tipos, chamadas **casting**.



**Conversão implícita**

* Ocorre automaticamente quando **não há perda de dados**

```csharp
int inteiro = 42;
double real = inteiro; // OK: int para double

```



**Conversão explícita**

* Exige uma conversão manual quando **há risco de perda de dados**.

```csharp
double real = 42.5;
int inteiro = (int)real; // Perde a parte decimal (42)

```



**Classe `Convert`**

* Para conversões seguras:

```csharp
string texto = "100";
int numero = Convert.ToInt32(texto);

```
