# Matrizes

#### 🔷 O que são matrizes em C#?

**Matrizes (arrays)** são estruturas que armazenam **coleções de elementos do mesmo tipo**, acessados por **índices numéricos**.

***

#### 🔹 Tipos de matrizes:

1.  **Matriz unidimensional (vetor)**\
    Declaração:

    ```csharp
    int[] numeros = new int[5]; // vetor com 5 elementos
    numeros[0] = 10;
    ```
2.  **Matriz bidimensional (tabela)**\
    Ex: uma tabela de 3 linhas e 4 colunas:

    ```csharp
    int[,] tabela = new int[3, 4];
    tabela[0, 0] = 1;
    ```
3.  **Matriz tridimensional**

    ```csharp
    int[,,] cubo = new int[2, 3, 4];
    ```
4.  **Array de arrays (jagged array)** – matriz com "linhas" de tamanhos diferentes

    ```csharp
    int[][] jagged = new int[3][];
    jagged[0] = new int[2]; // primeira linha com 2 colunas
    jagged[1] = new int[4]; // segunda linha com 4 colunas
    ```

***

#### 🔹 Principais propriedades e métodos:

*   `Length`: número total de elementos

    ```csharp
    int total = numeros.Length;
    ```
*   `GetLength(dimensão)`: tamanho em uma dimensão específica

    ```csharp
    int linhas = tabela.GetLength(0); // linhas
    int colunas = tabela.GetLength(1); // colunas
    ```

***

#### 🔹 Percorrendo matrizes:

**Unidimensional:**

```csharp
csharpCopyEditfor (int i = 0; i < numeros.Length; i++)
    Console.WriteLine(numeros[i]);
```

**Bidimensional:**

```csharp
csharpCopyEditfor (int i = 0; i < tabela.GetLength(0); i++)
    for (int j = 0; j < tabela.GetLength(1); j++)
        Console.WriteLine(tabela[i, j]);
```

***

#### 🔹 Inicialização rápida:

```csharp
csharpCopyEditint[] vet = { 1, 2, 3 };
int[,] mat = { { 1, 2 }, { 3, 4 } };
int[][] jagged = {
    new int[] { 1, 2 },
    new int[] { 3, 4, 5 }
};
```
