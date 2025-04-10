# Boxing e Unboxing

### 🔹 O que é _Boxing_?

> **Boxing** é o processo de **converter um tipo valor (como `int`, `double`, `bool`) em um `object`** (ou qualquer tipo _reference_ compatível).

#### ✅ Exemplo:

```csharp
int numero = 10;
object obj = numero; // Boxing
```

📦 Aqui o valor `10` (tipo `int`) é "encaixotado" em um `object`.

### 🔹 O que é _Unboxing_?

> **Unboxing** é o processo **inverso do boxing**: converter um `object` de volta para o tipo valor original.

#### ✅ Exemplo:

```csharp
object obj = 10;         // boxing
int numero = (int)obj;   // unboxing
```

🔁 Aqui o `object` volta a ser um `int`.

***

### ⚠️ Atenção:

* O _unboxing_ exige **casting explícito**.
* Se tentar fazer _unboxing_ para o tipo errado, ocorre **`InvalidCastException`**.

```csharp
 object obj = 10;
double d = (double)obj; // ERRO em tempo de execução!
```

***

### 🔸 Quando isso acontece na prática?

* Ao usar **coleções antigas** como `ArrayList`, que armazenam elementos como `object`.
* Ao passar tipos valor para APIs que esperam `object`.

***

### 🔹 Impacto em performance:

* _Boxing_ e _unboxing_ envolvem **cópia e alocação de memória no heap**, o que pode afetar a performance em cenários com muitas operações repetidas.

***

### ✅ Alternativas modernas:

Para evitar _boxing/unboxing_, prefira:

* **Genéricos (`List<T>`, `Dictionary<TKey, TValue>`)**
* **Tipos específicos**, evitando `object` quando possível
