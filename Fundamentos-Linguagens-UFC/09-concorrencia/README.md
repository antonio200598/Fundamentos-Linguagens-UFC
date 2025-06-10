# Desafio 09 – Concorrência

## 🎯 Objetivo

Explicar a diferença entre processos e threads, e implementar um exemplo de concorrência.

## 🧠 Conceito
- Processos e threads são dois conceitos fundamentais em sistemas operacionais que tratam da execução de programas, mas diferem em sua natureza, isolamento e gerenciamento. As suas principais diferenças são:
  
#### Thread:
  
- Definição: Uma thread é a menor unidade de execução dentro de um processo. Threads de um mesmo processo compartilham o mesmo espaço de memória, o que significa que podem acessar as mesmas variáveis, objetos e outros recursos.

-  Compartilhamento e Eficiência: Como as threads compartilham o mesmo ambiente, a comunicação entre elas é mais direta e eficiente em comparação com a comunicação interprocessual. Por outro lado, isso também implica riscos de inconsistências e a necessidade de sincronização, já que uma thread pode modificar dados que outra está utilizando.

-  Leveza: Criar e gerenciar threads geralmente envolve menos overhead do que criar processos, tornando-as uma opção mais leve para tarefas que podem ser executadas de forma concorrente dentro do mesmo processo.

#### Processo:

- Definição: Um processo é uma instância em execução de um programa. Cada processo possui seu próprio espaço de memória isolado, o que significa que o seu conjunto de variáveis, pilha e dados são privados e não podem ser acessados diretamente por outros processos.

- Isolamento: O isolamento entre processos garante que, se um processo falhar, ele não afete diretamente a execução de outros processos. Isso aumenta a estabilidade do sistema, mas também significa que a comunicação entre processos (usando técnicas como IPC — Inter-Process Communication) pode ser mais complexa e custosa.

- Recursos: Processos são geralmente mais pesados, pois criá-los e manter suas estruturas de gerenciamento (como tabelas de processos e alocação de espaço de memória) demandam mais recursos do sistema.

  
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
