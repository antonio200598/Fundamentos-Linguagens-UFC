# Desafio 04 – Tipos de Dados

## 🎯 Objetivo

Comparar a tipagem entre três linguagens diferentes, destacando diferenças entre tipagem estática, dinâmica e fraca.

## 🔍 Linguagens Escolhidas

- **Python** – Tipagem dinâmica e forte
- **C** – Tipagem estática e forte
- **JavaScript** – Tipagem dinâmica e fraca

## 🧪 Exemplos Comparativos

| Linguagem   | Declaração de Variável         | Observações                          |
|-------------|---------------------------------|--------------------------------------|
| Python      | `x = 10`                        | Tipo definido em tempo de execução   |
| C           | `int x = 10;`                   | Necessário declarar o tipo explicitamente |
| JavaScript  | `var x = 10;`                   | Tipo pode mudar dinamicamente        |

### 🧠 Considerações

- Em Python, variáveis não têm tipo fixo, mas não é permitido usar operações inválidas (`10 + "texto"` gera erro).
- Em C, o tipo é fixo, e mudanças exigem casting explícito.
- Em JavaScript, o tipo pode mudar e operar valores diferentes sem erro, mas pode gerar comportamentos inesperados.

## 📚 Referências

- Documentações oficiais das linguagens
- Sebesta, R. W. *Conceitos de Linguagens de Programação*
