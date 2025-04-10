# Modificador Ref e Out

### 🔹 `ref` (referência)

#### ✅ O que é:

Permite passar uma **referência de uma variável já inicializada** para um método. O método pode **ler e modificar** o valor original.

#### ✅ Regras:

* A variável **deve estar inicializada antes** de ser passada.
* O método pode **ler e alterar** o valor.

#### ✅ Exemplo:

```csharp
csharpCopyEditpublic void Dobrar(ref int numero)
{
    numero *= 2;
}

int valor = 5;
Dobrar(ref valor);
Console.WriteLine(valor); // Saída: 10
```

***

### 🔹 `out` (saída)

#### ✅ O que é:

Também passa uma variável **por referência**, mas é usada para **retornar múltiplos valores**. A variável **não precisa estar inicializada antes**, mas **precisa ser atribuída dentro do método**.

#### ✅ Regras:

* A variável **não precisa ser inicializada antes**.
* O método **é obrigado a atribuir um valor** à variável.

#### ✅ Exemplo:

```csharp
csharpCopyEditpublic void Dividir(int total, int divisor, out int resultado, out int resto)
{
    resultado = total / divisor;
    resto = total % divisor;
}

int r, s;
Dividir(10, 3, out r, out s);
Console.WriteLine($"Resultado: {r}, Resto: {s}"); // Saída: Resultado: 3, Resto: 1
```

***

### 🔸 Diferença entre `ref` e `out`:

| Característica                    | `ref`                        | `out`                      |
| --------------------------------- | ---------------------------- | -------------------------- |
| Precisa estar inicializada antes? | Sim                          | Não                        |
| Precisa ser atribuída no método?  | Não obrigatoriamente         | Sim                        |
| Usado para...                     | Modificar um valor existente | Retornar múltiplos valores |
