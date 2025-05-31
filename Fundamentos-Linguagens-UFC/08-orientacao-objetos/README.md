# Desafio 08 – Programação Orientada a Objetos

## 🎯 Objetivo

Criar uma hierarquia de classes utilizando conceitos de POO como herança e encapsulamento.

## 🎮 Tema: Personagens de Jogo

### Linguagem: Python

```python
class Personagem:
    def __init__(self, nome, vida):
        self.nome = nome
        self.vida = vida

    def atacar(self):
        return f"{self.nome} ataca!"

class Mago(Personagem):
    def __init__(self, nome, vida, mana):
        super().__init__(nome, vida)
        self.mana = mana

    def conjurar_feitico(self):
        return f"{self.nome} conjura um feitiço!"
