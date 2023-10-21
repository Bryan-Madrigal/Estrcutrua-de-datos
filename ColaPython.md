
MaxTamC = 10

# Inicializar la cola
frente = 0
final = 0
A = [0] * (MaxTamC + 1)
contador = 0

# Solicitar al usuario si desea agregar elementos a la cola
respuesta = input("Desea agregar elementos a la cola? (s/n): ")

while (respuesta == 's' or respuesta == 'S') and contador < MaxTamC:
    if (final + 1) % (MaxTamC + 1) == frente:
        print("Desbordamiento de la cola")
        exit(1)

    elemento = int(input("Ingrese un elemento para la cola: "))
    final = (final + 1) % (MaxTamC + 1)
    A[final] = elemento

    contador += 1
    print("Elemento {} agregado a la cola: {}".format(contador, elemento))

    if contador < MaxTamC:
        respuesta = input("Desea agregar mas elementos a la cola? (s/n): ")

# Validar si la cola está vacía
if frente == final:
    print("La cola esta vacia.")
    exit(1)

# Obtener el primer elemento de la cola
primerElemento = A[(frente + 1) % (MaxTamC + 1)]
print("El primer elemento de la cola es:", primerElemento)

# Eliminar un elemento de la cola
frente = (frente + 1) % (MaxTamC + 1)

# Imprimir elementos de la cola en el orden en que fueron ingresados
print("Elementos de la cola en el orden de ingreso:")
for i in range((frente + 1), (final + 1) % (MaxTamC + 1)):
    print(A[i], end=" ")
print()

