# DateTime

### ✅ **O que é `DateTime`?**

* `DateTime` é um **tipo de dado** usado para representar **datas e horas**.
* Pode armazenar: **ano, mês, dia, hora, minuto, segundo e milissegundo**.
* É uma **estrutura** (`struct`), e também **imutável** (como `string`).

***

### 🔹 **Principais formas de criar um `DateTime`**

| Como                       | Exemplo                     |
| -------------------------- | --------------------------- |
| Data e hora atual          | `DateTime.Now`              |
| Data atual (sem hora)      | `DateTime.Today`            |
| Hora UTC atual             | `DateTime.UtcNow`           |
| Criar uma data manualmente | `new DateTime(2024, 4, 27)` |

***

### 🔹 **Principais propriedades**

| Propriedade | O que retorna        | Exemplo                     |
| ----------- | -------------------- | --------------------------- |
| `Year`      | Ano                  | `data.Year → 2024`          |
| `Month`     | Mês                  | `data.Month → 4`            |
| `Day`       | Dia                  | `data.Day → 27`             |
| `Hour`      | Hora                 | `data.Hour → 14`            |
| `Minute`    | Minuto               | `data.Minute → 30`          |
| `Second`    | Segundo              | `data.Second → 45`          |
| `DayOfWeek` | Dia da semana        | `data.DayOfWeek → Saturday` |
| `DayOfYear` | Número do dia no ano | `data.DayOfYear → 118`      |

***

### 🔹 **Principais métodos**

| Método                     | O que faz                         | Exemplo                                   |
| -------------------------- | --------------------------------- | ----------------------------------------- |
| `AddDays(x)`               | Soma dias                         | `data.AddDays(5)` → +5 dias               |
| `AddHours(x)`              | Soma horas                        | `data.AddHours(2)` → +2 horas             |
| `AddMinutes(x)`            | Soma minutos                      | `data.AddMinutes(30)` → +30 minutos       |
| `Subtract(DateTime)`       | Diferença entre duas datas        | `data2.Subtract(data1)` → `TimeSpan`      |
| `Compare(d1, d2)`          | Compara duas datas                | `DateTime.Compare(d1, d2)` → -1, 0 ou 1   |
| `Equals(outro)`            | Verifica se são iguais            | `data1.Equals(data2)`                     |
| `ToString()`               | Converte em texto                 | `data.ToString()`                         |
| `Parse(string)`            | Converte texto para DateTime      | `DateTime.Parse("27/04/2024")`            |
| `TryParse(string, out dt)` | Tenta converter texto em DateTime | `DateTime.TryParse("data", out var data)` |
