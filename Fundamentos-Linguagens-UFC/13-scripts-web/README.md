# Desafio 13 – Linguagens para Scripts e Web

## 🎯 Objetivo

Criar um script para automação ou manipulação de dados usando uma linguagem de script.

## 💡 Linguagem Utilizada: Python

## 🛠️ Exemplo: Organizador de Arquivos por Extensão

```python
import os
import shutil

def organizar_pasta(diretorio):
    for arquivo in os.listdir(diretorio):
        nome, extensao = os.path.splitext(arquivo)
        if extensao:
            nova_pasta = os.path.join(diretorio, extensao[1:])
            os.makedirs(nova_pasta, exist_ok=True)
            shutil.move(os.path.join(diretorio, arquivo), os.path.join(nova_pasta, arquivo))

organizar_pasta("meus_arquivos")
