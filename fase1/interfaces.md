# Interfaces

Interfaces em C# são tipos que definem um **contrato**, ou seja, um conjunto de métodos, propriedades, eventos ou indexadores que uma classe ou struct deve implementar. As interfaces são amplamente utilizadas para fornecer flexibilidade, polimorfismo e para separar a definição de um comportamento da sua implementação.

***

### **1. O Que é uma Interface?**

* **Definição de Contrato**: Uma interface especifica quais membros (métodos, propriedades, etc.) uma classe deve implementar, mas **não contém implementação**.
* **Palavra-chave**: `interface`.
* **Polimorfismo**: Interfaces permitem que diferentes classes sejam tratadas de maneira uniforme.
* **Organização**: São úteis para organizar o código em sistemas complexos.

***

### **2. Criando uma Interface**

Uma interface é definida usando a palavra-chave `interface`. Seus membros **não têm corpo** e são implicitamente públicos e abstratos.

#### Exemplo de Interface:

```csharp
public interface IVeiculo
{
    void Acelerar(); // Método sem implementação
    void Frear();    // Outro método sem implementação
}
```

***

### **3. Implementando uma Interface**

Uma classe que implementa uma interface deve fornecer uma **implementação concreta** para todos os membros da interface.

#### Exemplo:

```csharp
public class Carro : IVeiculo
{
    public void Acelerar()
    {
        Console.WriteLine("O carro está acelerando...");
    }

    public void Frear()
    {
        Console.WriteLine("O carro está freando...");
    }
}
```

#### Uso:

```csharp
class Program
{
    static void Main()
    {
        IVeiculo veiculo = new Carro(); // Polimorfismo
        veiculo.Acelerar(); // Saída: O carro está acelerando...
        veiculo.Frear();    // Saída: O carro está freando...
    }
}
```
