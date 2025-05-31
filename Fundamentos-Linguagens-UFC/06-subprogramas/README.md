# Desafio 06 – Subprogramas

## 🎯 Objetivo

Demonstrar a passagem de parâmetros por valor e por referência.

## 🔍 Linguagens Usadas

- **C** (passagem por valor e ponteiro)
- **Python** (passagem por referência para objetos mutáveis)

### 🧪 Exemplo em C

```c
void incrementa(int x) {
    x++;
}

void incrementaRef(int* x) {
    (*x)++;
}
