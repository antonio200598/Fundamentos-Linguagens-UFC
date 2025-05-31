# Desafio 05 – Estruturas de Controle

## 🎯 Objetivo

Desenvolver um programa que utilize estruturas de seleção, repetição e controle de fluxo.

## 🖥️ Exemplo: Menu de Opções Bancárias em Python

```python
saldo = 1000

while True:
    print("1. Ver saldo")
    print("2. Depositar")
    print("3. Sair")
    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        print(f"Saldo atual: R$ {saldo}")
    elif opcao == "2":
        valor = float(input("Digite o valor a depositar: "))
        saldo += valor
    elif opcao == "3":
        break
    else:
        print("Opção inválida")
