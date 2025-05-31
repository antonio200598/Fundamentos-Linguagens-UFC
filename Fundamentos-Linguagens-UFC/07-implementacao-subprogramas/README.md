# Desafio 07 – Implementação de Subprogramas

## 🎯 Objetivo

Demonstrar como funciona a pilha de chamadas (call stack) através de um exemplo recursivo.

## 🖥️ Exemplo: Fatorial Recursivo em Python

```python
def fatorial(n):
    if n == 0 or n == 1:
        return 1
    return n * fatorial(n - 1)

print(fatorial(4))
