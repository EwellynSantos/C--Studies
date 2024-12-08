# Enums

um **enum** (abreviação de _enumeration_) é um tipo especial que permite definir um conjunto de valores constantes nomeados. Ele é usado para representar um grupo de opções ou categorias de maneira mais legível e segura no código.



### **1. Características do Enum**

* **Tipo por Valor**: Um `enum` é baseado em um tipo por valor, geralmente `int`.
* **Valores Nomeados**: Os elementos são constantes e têm um valor numérico associado.
* **Melhor Legibilidade**: Substitui o uso de números "mágicos" no código, tornando-o mais claro.
* **Seguro**: Restringe os valores permitidos a um conjunto fixo.



### **2. Definição de Enum**

A palavra-chave `enum` é usada para definir um tipo de enumeração.

#### **2.1. Sintaxe Básica**

```csharp
enum DiasDaSemana
{
    Domingo,
    Segunda,
    Terca,
    Quarta,
    Quinta,
    Sexta,
    Sabado
}
```

Por padrão:

* Os valores começam em 0 e são incrementados automaticamente.
  * `Domingo` será 0, `Segunda` será 1, e assim por diante.



### **3. Personalizando os Valores**

Você pode definir explicitamente os valores numéricos dos membros.

```csharp
enum NivelDeAcesso
{
    Usuario = 1,
    Moderador = 2,
    Administrador = 3
}
```



### **4. Usando um Enum**

#### **4.1. Declarando uma Variável Enum**

```csharp
DiasDaSemana hoje = DiasDaSemana.Sexta;
Console.WriteLine(hoje); // Saída: Sexta
```

#### **4.2. Obtendo o Valor Numérico**

Você pode converter um enum em seu valor numérico correspondente com `(int)`.

```csharp
int valor = (int)DiasDaSemana.Sexta;
Console.WriteLine(valor); // Saída: 5
```
