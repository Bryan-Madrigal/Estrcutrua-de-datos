//3J-LSC-BryanPerez

class Nodo:
    def __init__(self, dato):
        self.dato = dato
        self.siguiente = None

def agregar_nodo(cabeza, valor):
    nuevo_nodo = Nodo(valor)
    if cabeza is None:
        cabeza = nuevo_nodo
        return cabeza
    else:
        actual = cabeza
        while actual.siguiente is not None:
            actual = actual.siguiente
        actual.siguiente = nuevo_nodo
        return cabeza

def imprimir_lista(cabeza):
    actual = cabeza
    while actual is not None:
        print(actual.dato, end=' ')
        actual = actual.siguiente
    print()

def borrar_lista(cabeza):
    while cabeza is not None:
        siguiente = cabeza.siguiente
        del cabeza
        cabeza = siguiente
    return None

if __name__ == "__main__":
    cabeza = None
    tamano_lista = int(input("Ingrese la cantidad de elementos que desea agregar a la lista: "))

    if tamano_lista <= 0:
        print("Cantidad de elementos no valida.")
    else:
        for i in range(tamano_lista):
            valor = int(input(f"Ingrese dato {i + 1}: "))
            cabeza = agregar_nodo(cabeza, valor)

        print("Imprimiendo lista de numeros")
        imprimir_lista(cabeza)

        cabeza = borrar_lista(cabeza)
