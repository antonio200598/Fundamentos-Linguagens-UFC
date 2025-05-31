# Desafio 10 – Gerenciamento de Memória

## 🎯 Objetivo

Comparar como a memória é gerenciada em duas linguagens com abordagens distintas: manual e automática.

## 🔍 Linguagens

- **C** – Gerenciamento manual
- **Java** – Coleta de lixo (Garbage Collection)

## 🧪 Comparativo

| Característica              | C                         | Java                     |
|-----------------------------|---------------------------|--------------------------|
| Alocação de memória         | Manual (`malloc`)         | Automática (`new`)       |
| Liberação de memória        | Manual (`free`)           | Coletor de lixo (GC)     |
| Risco de vazamento          | Alto                      | Baixo                    |
| Controle pelo programador   | Total                     | Parcial                  |

### 🧠 Considerações

- Em C, o programador é responsável por alocar e liberar memória. Um erro pode causar vazamento ou corrupção de dados.
- Em Java, a JVM executa um coletor de lixo que libera memória automaticamente, reduzindo erros, mas com custo em performance.

## 📚 Referência

- K&R C
- Java Platform Specification
- Sebesta, R. W. *Conceitos de Linguagens de Programação*
