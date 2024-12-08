---
description: >-
  Em C#, um struct (abreviação de structure) é um tipo de dado que permite
  agrupar variáveis relacionadas em uma única unidade, similar a uma classe, mas
  com diferenças importantes no comportamento e no
---

# Structs

### **1. Características Principais de Structs**

* **Tipo por Valor**: Structs são armazenados na _stack_ e possuem comportamento de tipos por valor. Isso significa que, ao atribuir um `struct` a outra variável, uma cópia é criada.
* **Mais Leves**: São ideais para representar objetos pequenos que possuem uma vida útil curta e não precisam de herança.
* **Sem Herança**: Não podem herdar de outras classes ou structs, mas podem implementar interfaces.
* **Imutabilidade Recomendada**: Structs geralmente são usados de forma imutável para evitar problemas relacionados a cópias.

### **2. Quando Usar Structs?**

* Para representar pequenas entidades, como pontos, coordenadas ou intervalos de tempo.
* Quando não há necessidade de herança.
* Quando o desempenho é crítico e o comportamento por valor é desejado.

Exemplos comuns:

* `System.DateTime`
* `System.TimeSpan`
* `System.Decimal`



### **3. Definição de um Struct**

#### **3.1. Sintaxe Básica**

```csharp
struct Ponto
{
    public int X;
    public int Y;

    public Ponto(int x, int y) // Construtor
    {
        X = x;
        Y = y;
    }

    public void MostrarCoordenadas()
    {
        Console.WriteLine($"Coordenadas: ({X}, {Y})");
    }
}

```



### **4. Criando e Usando um Struct**

#### **4.1. Criando uma Instância**

```csharp
Ponto p1 = new Ponto(10, 20);
p1.MostrarCoordenadas(); // Saída: Coordenadas: (10, 20)
```
