# List

### 🔹 O que é `List`?

`List<T>` é uma **coleção genérica** da biblioteca .NET que **armazena elementos em ordem** e permite acesso por índice. É como um **array dinâmico**, ou seja, cresce conforme os itens são adicionados.

***

### 🔹 Lista é uma estrutura de dados:

* Homogênea (dados so mesmo tipo)
* Ordenada (elementos acessados por meio de posições)
* Inicia vazia e seus elementos são alocados sob demanda
* Cada elemento ocupa um "nó" (iu nodo) da lista



### 🔹 Vantagens:

* Tamanaho variável
* Facilicade dpara se realizar inserçoes e deleções



### 🔹 Desvantagens:

* Acesso sequencial aos elementos



### 🔹 Sintaxe básica:

```csharp
List<int> numeros = new List<int>();
```

Você pode usar qualquer tipo no lugar de `int`, como `string`, `double`, objetos, etc.

Exemplo de lista já contendo valores:

```csharp
List<string> numeros = new List<string>{"Ana", "Rafael"};
```

***

### 🔹 Principais métodos:

| Método                | Descrição                         |
| --------------------- | --------------------------------- |
| `Add(item)`           | Adiciona um item                  |
| `Remove(item)`        | Remove o item especificado        |
| `RemoveAt(index)`     | Remove item pelo índice           |
| `Clear()`             | Remove todos os itens             |
| `Contains(item)`      | Verifica se o item existe         |
| `IndexOf(item)`       | Retorna o índice do item          |
| `Count`               | Quantidade de itens               |
| `Insert(index, item)` | Insere item na posição específica |
| `Sort()`              | Ordena a lista                    |
| `ForEach(action)`     | Executa uma ação para cada item   |

***

### 🔹 Exemplo simples:

```csharp
csharpCopyEditList<string> nomes = new List<string>();
nomes.Add("Ana");
nomes.Add("Lucas");
nomes.Add("Maria");

foreach (var nome in nomes)
{
    Console.WriteLine(nome);
}
```

***

### 🔹 Diferença entre `List` e `Array`:

| Característica      | `List<T>` | `Array`          |
| ------------------- | --------- | ---------------- |
| Tamanho             | Dinâmico  | Fixo             |
| Métodos disponíveis | Muitos    | Poucos           |
| Tipo                | Genérico  | Genérico ou fixo |



#### ✅ `Add()`

```csharp
csharpCopyEditList<string> frutas = new List<string>();
frutas.Add("Maçã");
frutas.Add("Banana");

Console.WriteLine(string.Join(", ", frutas)); // Saída: Maçã, Banana
```

***

#### ✅ `Remove()`

```csharp
csharpCopyEditfrutas.Remove("Maçã");

Console.WriteLine(string.Join(", ", frutas)); // Saída: Banana
```

***

#### ✅ `RemoveAt(index)`

```csharp
csharpCopyEditfrutas.Add("Laranja");
frutas.RemoveAt(1); // Remove o item no índice 1 ("Laranja")

Console.WriteLine(string.Join(", ", frutas)); // Saída: Banana
```

***

#### ✅ `Insert(index, item)`

```csharp
csharpCopyEditfrutas.Insert(0, "Uva");

Console.WriteLine(string.Join(", ", frutas)); // Saída: Uva, Banana
```

***

#### ✅ `Contains()`

```csharp
csharpCopyEditbool temBanana = frutas.Contains("Banana");

Console.WriteLine(temBanana); // Saída: True
```

***

#### ✅ `IndexOf()`

```csharp
csharpCopyEditint indice = frutas.IndexOf("Banana");

Console.WriteLine(indice); // Saída: 1
```

***

#### ✅ `Sort()`

```csharp
csharpCopyEditList<int> numeros = new List<int> { 3, 1, 4, 2 };
numeros.Sort();

Console.WriteLine(string.Join(", ", numeros)); // Saída: 1, 2, 3, 4
```

***

#### ✅ `Clear()`

```csharp
csharpCopyEditnumeros.Clear();

Console.WriteLine(numeros.Count); // Saída: 0
```

***

#### ✅ `ForEach()`

```csharp
csharpCopyEditList<string> nomes = new List<string> { "Ana", "João", "Carlos" };

nomes.ForEach(nome => Console.WriteLine("Olá, " + nome));
// Saída:
// Olá, Ana
// Olá, João
// Olá, Carlos
```
