# Vetores/Arrays

Em C#, um **vetor** (_array_) é uma estrutura de dados que armazena múltiplos valores do mesmo tipo em uma sequência ordenada. Ele possui um tamanho fixo, definido no momento da sua criação.

#### Declaração e Inicialização

Você pode declarar e inicializar um vetor de várias formas:

```csharp
// Declaração e inicialização com tamanho fixo
int[] numeros = new int[5]; // Vetor de 5 posições

// Inicialização direta com valores
string[] nomes = { "Ana", "Carlos", "Bruna" };

// Outra forma de inicializar
int[] idades = new int[] { 25, 30, 22, 28 };
```

#### Métodos Úteis

A classe `Array` fornece métodos úteis, como:

```csharp
Array.Sort(numeros);  // Ordena o vetor
Array.Reverse(numeros); // Inverte a ordem dos elementos
int tamanho = numeros.Length; // Retorna o tamanho do vetor
```

#### Observação

* O tamanho do vetor é fixo; se precisar de uma estrutura dinâmica, use `List<T>`.
* Caso tente acessar um índice inválido (`numeros[10]` em um vetor de tamanho 5), ocorrerá uma exceção `IndexOutOfRangeException`.
