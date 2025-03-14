# Desalicação de memória: Garbage Collector e Escopo Local

#### 🗑 **Garbage Collector (GC)**

O **Garbage Collector** é o mecanismo do .NET responsável por **gerenciar a memória automaticamente**, evitando vazamentos de memória. Ele libera memória de objetos que **não estão mais sendo referenciados** pelo programa.

**🔄 Como funciona o GC?**

1. **Alocação de Memória**: Quando você cria um objeto (ex: `new MinhaClasse()`), ele é armazenado no **heap gerenciado**.
2. **Coleta de Lixo**:
   * O GC monitora objetos que **não estão mais acessíveis**.
   * Quando necessário, ele libera memória desses objetos.
   * O processo ocorre em **três gerações** (Gen 0, Gen 1 e Gen 2), onde objetos mais antigos são coletados com menos frequência.
3. **Finalizadores e IDisposable**:
   * O GC pode chamar um método `Finalize()`, mas o ideal é **evitar dependência disso**.
   * Para liberar recursos como conexões de banco ou arquivos, implemente **`IDisposable`** e use `Dispose()` ou `using`..



#### 🏠 **Escopo Local e Desalocação em C#**

O **escopo local** em C# refere-se a variáveis que existem **apenas dentro de um bloco de código**, como dentro de um método.

**🛑 Como a memória é desalocada?**

* **Variáveis locais (stack)**:
  * São desalocadas automaticamente quando o escopo do método termina.
  *   Exemplo:

      ```csharp
      csharpCopyEditvoid MeuMetodo()
      {
          int x = 10; // Alocada na stack, removida ao sair do método
      } // Aqui, x é desalocado automaticamente
      ```
* **Objetos no heap (GC)**:
  * Criados com `new`, permanecem na memória até o GC coletá-los.
  *   Exemplo:

      ```csharp
      csharpCopyEditvoid CriarObjeto()
      {
          MinhaClasse obj = new MinhaClasse(); // Alocado no heap
      } // Aqui, a referência some, mas o GC decidirá quando liberar
      ```
* **`using` para liberar recursos imediatamente**:
  *   Se um objeto implementa `IDisposable`, use `using` para garantir que ele seja liberado corretamente:

      ```csharp
      csharpCopyEditusing (var stream = new FileStream("arquivo.txt", FileMode.Open))
      {
          // Usa o arquivo
      } // Aqui, o GC chama Dispose() automaticamente
      ```

#### 🎯 **Resumindo**

✔ **Garbage Collector** gerencia a memória automaticamente.\
✔ **Variáveis locais são desalocadas ao sair do escopo**.\
✔ **Objetos no heap são coletados pelo GC quando não há mais referências**.\
✔ **Recursos não gerenciados (arquivos, conexões) devem ser liberados manualmente com `Dispose()` ou `using`**.

