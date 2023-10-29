# Funcion para imprimir la tabla de multiplicar con un bucle while
def tabla_de_multiplicar():
    NUM = int(input("Digite numero: "))

    I = 1
    while I <= 12:
        RESUL = NUM * I
        print(f"{NUM} * {I} = {RESUL}")
        I += 1

    input("Pulse una Tecla:")

if __name__ == "__main__":
    tabla_de_multiplicar()

