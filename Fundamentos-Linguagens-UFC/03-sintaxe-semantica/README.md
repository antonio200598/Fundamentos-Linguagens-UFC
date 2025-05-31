# Desafio 03 – Descrições Sintáticas e Semânticas

## 🎯 Objetivo

Criar uma mini-gramática de uma linguagem fictícia, demonstrando noções de análise léxica, regras sintáticas (como BNF) e interpretação básica de comandos simples.

## 💡 Linguagem Fictícia: MiniLang

MiniLang é uma linguagem fictícia com sintaxe simples voltada para ilustrar os conceitos básicos de análise léxica, sintática e semântica. Ela permite declarar variáveis inteiras e imprimir valores.

---

## 🔤 Análise Léxica (Tokens)

| Token     | Descrição                        | Exemplo      |
|-----------|----------------------------------|--------------|
| `INT`     | Palavra-chave para inteiros      | `INT`        |
| `PRINT`   | Comando de impressão             | `PRINT`      |
| `id`      | Identificador (nome de variável) | `x`, `nome`  |
| `num`     | Número inteiro                   | `42`, `7`    |
| `=`       | Operador de atribuição           | `=`          |
| `;`       | Delimitador de comando           | `;`          |

---

## 📐 Regras Sintáticas (BNF simplificado)

```bnf
<programa>   ::= <comando> | <comando> <programa>
<comando>    ::= <decl> | <impressao>
<decl>       ::= 'INT' <id> '=' <num> ';'
<impressao>  ::= 'PRINT' <id> ';'
<id>         ::= letra {letra | digito}
<num>        ::= dígito {dígito}
