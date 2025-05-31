# Desafio 12 – Programação Lógica

## 🎯 Objetivo

Modelar um pequeno problema usando regras lógicas inspiradas em Prolog.

## 🔍 Tema: Genealogia

```prolog
pai(joao, maria).
pai(joao, jose).
mae(ana, maria).
mae(ana, jose).

irmao(X, Y) :- pai(P, X), pai(P, Y), mae(M, X), mae(M, Y), X \= Y.
