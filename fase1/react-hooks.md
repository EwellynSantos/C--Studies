# React Hooks

### ⚛️ **O que são React Hooks?**

**Hooks** são **funções do React** que permitem **usar estado e outras funcionalidades do React** em **componentes funcionais**, sem precisar usar classes.

Introduzidos no **React 16.8**, os hooks tornaram possível escrever componentes **mais simples, reutilizáveis e legíveis**.

***

### 🔑 **Por que usar Hooks?**

* Substituem componentes de classe na maioria dos casos
* Permitem **reutilizar lógica de estado** (com _custom hooks_)
* Melhor legibilidade e organização do código
* Facilitam **testes e manutenção**

***

### 🎣 Principais Hooks do React

#### 1. **`useState`** — Gerencia estado local

```tsx
tsxCopyEditconst [contador, setContador] = useState(0);

setContador(contador + 1);
```

***

#### 2. **`useEffect`** — Executa efeitos colaterais (ex: requisições, timers)

```tsx
tsxCopyEdituseEffect(() => {
  console.log("Componente montou");

  return () => console.log("Componente desmontou");
}, []);
```

* `[]` = executa **apenas uma vez** (como `componentDidMount`)
* `[variavel]` = executa sempre que a variável mudar

***

#### 3. **`useContext`** — Acessa dados de um **Context API**

```tsx
tsxCopyEditconst tema = useContext(TemaContext);
```

***

#### 4. **`useRef`** — Referência mutável (sem rerender)

```tsx
tsxCopyEditconst inputRef = useRef<HTMLInputElement>(null);

<input ref={inputRef} />
```

***

#### 5. **`useMemo`** — **Memoriza cálculos pesados**

```tsx
tsxCopyEditconst resultado = useMemo(() => calcularAlgo(dado), [dado]);
```

***

#### 6. **`useCallback`** — Memoriza funções (evita recriação desnecessária)

```tsx
tsxCopyEditconst handleClick = useCallback(() => {
  console.log("clicou");
}, []);
```

***

#### 7. **`useReducer`** — Alternativa ao useState para estados mais complexos

```tsx
tsxCopyEditconst [estado, dispatch] = useReducer(reducer, estadoInicial);
```

***

#### 8. **`useLayoutEffect`** — Como o `useEffect`, mas executa **antes da pintura da tela** (⚠️ uso avançado)

***

#### 9. **`useImperativeHandle`** — Personaliza o que será exposto via `ref` em componentes personalizados (⚙️ avançado)&#x20;
