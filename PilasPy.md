capacidad = 10
elementos = []

print("Teclea elemento de la pila (termina con -1)")

while len(elementos) < capacidad:
    entrada = input()

    if entrada == '-1':
        break

    if entrada.isdigit():
        x = int(entrada)
        elementos.append(x)
    else:
        print("Excepcion: Entrada no valida")

print("Elementos de la Pila:", end=" ")
print(*elementos[::-1])
