import random

# Genera un número aleatorio entre 1 y 100
numero_ganador = random.randint(1, 100)
intentos = 10

print("¡Adivina el número y gana! Tienes 10 intentos.")

# Solicita al usuario ingresar un número
numero = int(input("Ingresa un número entre 1 y 100: "))

# Bucle que continúa hasta que el número adivinado sea correcto
while numero != numero_ganador and intentos > 1:
    if numero > numero_ganador:
        print("Busca un número menor.")
    elif numero < numero_ganador:
        print("Busca un número mayor.")
    
    intentos -= 1
 
 # Solicita al usuario ingresar otro número
    numero = int(input(f"Te quedan {intentos} intentos. Ingresa otro número: "))

# Mensaje de éxito o derrota cuando adivina el número
if numero == numero_ganador:
    print("¡Felicidades! ¡Ganaste!")
else:
    print(f"¡Perdiste! El número correcto era {numero_ganador}.")
