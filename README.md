Bryan Raul Perez Madrigal-3J-LSC

#include <iostream>
using namespace std;

const int NUM = 8;

int main() {
    int nums[NUM];
    int total = 0;

    for (int i = 0; i < NUM; i++) {
        cout << "Por favor, introduzca el número: ";
        cin >> nums[i];
        total += nums[i];
    }

    cout << "El total de números es: " << total << endl;
    
    return 0;
}
