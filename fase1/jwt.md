# JWT

### 🔐 **O que é JWT?**

**JWT (JSON Web Token)** é um **formato de token** usado para **autenticação e troca segura de informações** entre partes, geralmente entre o frontend e o backend.

É um **token compactado e assinado**, que pode ser verificado, mas **não é criptografado por padrão**.

***

### 🧱 **Como é a estrutura do JWT?**

Um token JWT tem **3 partes**, separadas por pontos (`.`):

```
CopyEditxxxxx.yyyyy.zzzzz
```

<table><thead><tr><th width="112">Parte</th><th width="114">Nome</th><th>Função</th></tr></thead><tbody><tr><td><strong>Header</strong></td><td>Cabeçalho</td><td>Define o tipo de token (JWT) e o algoritmo de assinatura (ex: HS256)</td></tr><tr><td><strong>Payload</strong></td><td>Corpo</td><td>Contém os <strong>dados</strong> (ex: ID do usuário, permissões, etc)</td></tr><tr><td><strong>Signature</strong></td><td>Assinatura</td><td>Garante que o conteúdo <strong>não foi alterado</strong></td></tr></tbody></table>

***

#### 📦 Exemplo de Payload (dados do token):

```json
jsonCopyEdit{
  "sub": "1234567890",
  "name": "João Silva",
  "role": "admin",
  "iat": 1715550000,
  "exp": 1715553600
}
```

***

### 🔁 **Como funciona na prática?**

1. **Usuário faz login** (envia e-mail e senha)
2. Backend **valida** os dados e **gera um JWT**
3. O frontend **armazena** o JWT (geralmente no `localStorage` ou `sessionStorage`)
4. Em cada requisição futura, o JWT é enviado no **header**:

```
makefileCopyEditAuthorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI...
```

5. O backend **valida o token** antes de responder

***

### ✅ Vantagens do JWT

* **Stateless**: o servidor **não precisa manter sessão**
* **Compacto**: ideal para ser enviado via HTTP
* **Seguro**: é **assinado** (não pode ser alterado sem invalidar a assinatura)
* **Autocontido**: carrega as **informações do usuário** dentro do próprio token

***

### ⚠️ Cuidados importantes

* **Não armazene dados sensíveis** no payload (não é criptografado por padrão)
* Sempre use **HTTPS**
* Use **tempo de expiração (`exp`) curto**
* Pode ser invalidado com **blacklist** em sistemas críticos
