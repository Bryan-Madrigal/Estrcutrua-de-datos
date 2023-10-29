#include <iostream>
using namespace std;

// Funcion para la suma de digitos de forma iterativa
int sumaIterativa(int n) {
    int suma = 0;

    while (n > 9) {
        suma += n % 10;
        n /= 10;
    }

    return (suma + n);
}

// Funcion para la suma de digitos de forma recursiva
int sumaRecursiva(int n) {
    if (n <= 9)
        return n;
    else
        return sumaRecursiva(n / 10) + n % 10;
}

int main() {
    int numero;
    cout << "Ingresa un numero entero: ";
    cin >> numero;

    int resultadoIterativo = sumaIterativa(numero);
    int resultadoRecursivo = sumaRecursiva(numero);

    cout << "Suma de los digitos de manera iterativa: " << resultadoIterativo << endl;
    cout << "Suma de los digitos de manera recursiva: " << resultadoRecursivo << endl;

    return 0;
}
