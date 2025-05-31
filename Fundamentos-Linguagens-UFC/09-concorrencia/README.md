# Desafio 09 – Concorrência

## 🎯 Objetivo

Explicar a diferença entre processos e threads, e implementar um exemplo de concorrência.

## 🧠 Conceito

- **Thread:** Compartilha memória com outras threads no mesmo processo.
- **Processo:** Executa de forma independente, com seu próprio espaço de memória.

## 🧪 Exemplo em Python (Threading)

```python
import threading
import time

def tarefa(nome):
    print(f"Iniciando {nome}")
    time.sleep(2)
    print(f"Finalizando {nome}")

t1 = threading.Thread(target=tarefa, args=("T1",))
t2 = threading.Thread(target=tarefa, args=("T2",))

t1.start()
t2.start()

t1.join()
t2.join()
