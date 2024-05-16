import random

numero_secreto = random.randint(1, 100)
tentativas = 0

print("Bem-vindo ao jogo de adivinhação!")
print("Tente adivinhar o número entre 1 e 100.")

while True:
    palpite = int(input("Digite seu palpite: "))
    
    # Contador de tentativas
    tentativas += 1
    
    # Verificando se o palpite está correto
    if palpite == numero_secreto:
        print(f"Parabéns! Você acertou o número em {tentativas} tentativas.")
        break
    
    # Está quente ou frio
    # Quente como perto e frio como longe
    if abs(palpite - numero_secreto) < 20:
        print("Tá quente!")
    else:
        print("Tá frio!")
    
    # Está muito alto ou muito baixo
    if palpite < numero_secreto:
        print("Aumente mais a temperatura.")
    else:
        print("Abaixe mais a temperatura.")
