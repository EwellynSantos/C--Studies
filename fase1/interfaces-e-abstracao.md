# Interfaces e Abstração

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





### Abstração no C\#

A **abstração** é um dos pilares fundamentais da **Programação Orientada a Objetos (POO)**. Ela se refere ao processo de ocultar os detalhes de implementação de um objeto e expor apenas as funcionalidades essenciais para o mundo externo. Em outras palavras, abstração foca no _o que um objeto faz_, e não em _como ele faz_.

***

### **1. Objetivo da Abstração**

* Simplificar a interação com objetos complexos, expondo apenas o necessário.
* Reduzir a complexidade do código ao ocultar os detalhes de implementação.
* Facilitar a reutilização e a manutenção do código.

***

### **2. Implementando Abstração no C#**

No C#, a abstração é implementada por meio de **classes abstratas** e **interfaces**.

#### **Classe Abstrata**

Uma **classe abstrata** é uma classe que não pode ser instanciada diretamente. Ela serve como uma base para outras classes, fornecendo uma implementação parcial ou apenas definindo membros que devem ser implementados pelas classes derivadas.

***

#### **Sintaxe e Exemplo**

**Classe Abstrata:**

```csharp
public abstract class Forma
{
    public string Cor { get; set; }

    // Método abstrato (não possui implementação)
    public abstract double CalcularArea();

    // Método concreto (possui implementação)
    public void Desenhar()
    {
        Console.WriteLine("Desenhando uma forma...");
    }
}

// Classe derivada
public class Circulo : Forma
{
    public double Raio { get; set; }

    public override double CalcularArea()
    {
        return Math.PI * Raio * Raio;
    }
}

// Outra classe derivada
public class Retangulo : Forma
{
    public double Largura { get; set; }
    public double Altura { get; set; }

    public override double CalcularArea()
    {
        return Largura * Altura;
    }
}
```

***

#### **Uso da Classe Abstrata**

```csharp
class Program
{
    static void Main()
    {
        Forma forma1 = new Circulo { Raio = 5, Cor = "Azul" };
        Forma forma2 = new Retangulo { Largura = 4, Altura = 6, Cor = "Vermelho" };

        Console.WriteLine($"Área do círculo: {forma1.CalcularArea()}"); // Área do círculo: 78.54
        Console.WriteLine($"Área do retângulo: {forma2.CalcularArea()}"); // Área do retângulo: 24
    }
}
```

***

### **3. Diferença entre Classe Abstrata e Interface**

| **Aspecto**      | **Classe Abstrata**                                | **Interface**                                                                 |
| ---------------- | -------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Herança**      | Uma classe pode herdar apenas uma classe abstrata. | Uma classe pode implementar várias interfaces.                                |
| **Métodos**      | Pode conter métodos concretos e abstratos.         | Apenas membros abstratos (antes do C# 8) ou com implementação padrão (C# 8+). |
| **Construtores** | Pode ter construtores.                             | Não pode ter construtores.                                                    |
| **Uso**          | Usada quando há uma relação "é um" (herança).      | Usada quando há uma relação "faz algo" (comportamentos).                      |

***

### **4. Abstração com Interfaces**

Enquanto as classes abstratas podem definir comportamento comum, as **interfaces** são usadas para definir contratos, permitindo que diferentes classes implementem o mesmo conjunto de funcionalidades.

#### Exemplo:

```csharp
public interface IVeiculo
{
    void Acelerar();
    void Frear();
}

public class Carro : IVeiculo
{
    public void Acelerar()
    {
        Console.WriteLine("Carro acelerando...");
    }

    public void Frear()
    {
        Console.WriteLine("Carro freando...");
    }
}

public class Bicicleta : IVeiculo
{
    public void Acelerar()
    {
        Console.WriteLine("Bicicleta acelerando...");
    }

    public void Frear()
    {
        Console.WriteLine("Bicicleta freando...");
    }
}
```

#### Uso:

```csharp
class Program
{
    static void Main()
    {
        IVeiculo veiculo1 = new Carro();
        IVeiculo veiculo2 = new Bicicleta();

        veiculo1.Acelerar(); // Saída: Carro acelerando...
        veiculo2.Frear();    // Saída: Bicicleta freando...
    }
}
```

***

### **5. Benefícios da Abstração**

1. **Reduz Complexidade**: Oculta detalhes desnecessários, expondo apenas o essencial.
2. **Flexibilidade**: Permite mudar a implementação interna sem afetar o código externo.
3. **Manutenibilidade**: Facilita a modificação e a extensão do código.
4. **Reutilização**: Classes e interfaces abstratas podem ser reutilizadas em diferentes cenários.
