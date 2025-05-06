# Timespan

#### 🔹 O que é `TimeSpan`?

`TimeSpan` é uma **estrutura (struct)** do .NET usada para **representar um intervalo de tempo**, como a diferença entre duas datas ou um período de duração (por exemplo, 2 horas e 30 minutos).

***

#### 🔹 Principais características:

* Representa tempo em **dias, horas, minutos, segundos e milissegundos**.
* Pode ser **positivo ou negativo**.
* Muito usado para **subtrair datas**, medir **duração de eventos** ou criar **delays**.

***

#### 🔹 Como criar um `TimeSpan`:

```csharp
csharpCopyEditTimeSpan ts1 = new TimeSpan(2, 30, 0); // 2h30min
TimeSpan ts2 = TimeSpan.FromHours(1.5); // 1h30min
TimeSpan ts3 = TimeSpan.FromDays(1); // 1 dia
```

***

#### 🔹 Operações com `TimeSpan`:

```csharp
csharpCopyEditTimeSpan ts1 = TimeSpan.FromHours(3);
TimeSpan ts2 = TimeSpan.FromHours(1);

TimeSpan soma = ts1 + ts2;       // 4 horas
TimeSpan subtracao = ts1 - ts2;  // 2 horas
```

***

#### 🔹 Comparação de `TimeSpan`:

```csharp
csharpCopyEditif (ts1 > ts2) { ... }
if (ts1 == ts2) { ... }
```

***

#### 🔹 Usando com `DateTime`:

```csharp
csharpCopyEditDateTime inicio = DateTime.Now;
DateTime fim = inicio.AddHours(2);
TimeSpan duracao = fim - inicio; // resultado: 2 horas
```

***

#### 🔹 Propriedades úteis:

* `TimeSpan.Days`
* `TimeSpan.Hours`
* `TimeSpan.Minutes`
* `TimeSpan.TotalHours` → retorna tudo convertido para horas (decimal)
* `TimeSpan.TotalMilliseconds` → retorna o total em milissegundos
