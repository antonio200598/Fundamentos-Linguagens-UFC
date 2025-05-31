# Desafio 11 – Programação Funcional

## 🎯 Objetivo

Implementar uma solução utilizando recursão e funções de alta ordem.

## 🖥️ Exemplo: Soma dos Números Pares

```python
from functools import reduce

numeros = list(range(1, 11))

pares = list(filter(lambda x: x % 2 == 0, numeros))
soma = reduce(lambda a, b: a + b, pares)

print(f"Soma dos pares: {soma}")

🧠 Alternativa Recursiva

def soma_pares(n):
    if n == 0:
        return 0
    return (n if n % 2 == 0 else 0) + soma_pares(n - 1)

print(soma_pares(10))
