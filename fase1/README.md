---
description: >-
  É um espaço na memória do pc para armazenar dados. Pra C#, podemos declarar
  variaveis vaziase elas podem ser alteradas em tempo de execução. Sintaxe:
---

# Variaveis

```csharp
tipo nomeVariavel; ou tipo nomeVariavel = valor;
```



### Tipos

Os **tipos de valor** armazenam os dados diretamente na memória. Eles são usados para tipos simples como números e booleanos.

<table><thead><tr><th width="137">Tipo</th><th width="263">Descrição</th><th>Exemplo </th></tr></thead><tbody><tr><td>Int </td><td>Valores inteiros</td><td>int i = 42;</td></tr><tr><td>float</td><td>números decimais (precisão de 7 dígitos)</td><td>float f = 3.14f;</td></tr><tr><td>double</td><td>números decimais (precisão de 15-16 dígitos)</td><td>double d = 3.14159;</td></tr><tr><td>decimal</td><td>números decimais (precisão de 28-29 dígitos)</td><td>decimal m = 3.14m;</td></tr><tr><td>bool</td><td>valores V ou F</td><td>bool isValid = true;</td></tr><tr><td>char</td><td>Qualquer caractere Unicode</td><td>char c = 'A';</td></tr></tbody></table>



### Tipo de Referência

Os **tipos de referência** armazenam um **endereço de memória**, e não o dado diretamente. São usados para objetos complexos e strings.



<table><thead><tr><th width="115">Tipo</th><th width="256">Descrição</th><th>Exemplo</th></tr></thead><tbody><tr><td>string</td><td>Sequencia de caracteres</td><td>string nome = "Maria";</td></tr><tr><td>object</td><td>Tipo base para todos os tipos</td><td>object obj = 42;</td></tr><tr><td>dynamic</td><td>Tipo que aceita valores dinâmicos</td><td>dynamic dyn = "texto";</td></tr><tr><td>Classes e Arrays</td><td>Objetos e coleções de valores</td><td>int[] numeros = {1, 2, 3};</td></tr></tbody></table>

**Importante:**

* **Strings** são imutáveis: uma vez criadas, não podem ser alteradas diretamente.
* **Dynamic** é útil, mas cuidado! Não tem verificação em tempo de compilação.





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
