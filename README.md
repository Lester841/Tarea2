# Tarea2
Tarea de algoritmos 2
Algoritmo TrianguloRectangulos
    Definir opciones, num, i, j Como Entero
    
    Escribir "Hola!, Porfavor ingresa un número entero positivo:"
    Leer num
    
    Si num > 0 Entonces
        Escribir "selecciona un numero :"
        Escribir "#1."
        Escribir "#2."
        Escribir "#3."
        Escribir "#4."
        
        Leer opciones
        
        Si opc >= 1 y opc <= 4 Entonces
            Para i = 1 Hasta num Hacer
                Si opc = 1 Entonces
                    Para j = 1 Hasta i Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Si opc = 2 Entonces
                    Para j = 1 Hasta num - i + 1 Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Si opc = 3 Entonces
                    Para j = 1 Hasta num - i Hacer
                        Escribir SinSaltar " ";
                    Fin Para
                    Para j = 1 Hasta i Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Si opc = 4 Entonces
                    Para j = 1 Hasta i - 1 Hacer
                        Escribir SinSaltar " ";
                    Fin Para
                    Para j = 1 Hasta num - i + 1 Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Escribir "";  
            Fin Para
        Fin Si
    Fin Si
	
Fin Algoritmo 


c++ 
#include <iostream>

using namespace std;

void dibujarTriangulo(int base, char caracter) {
    for (int i = 1; i <= base; i++) {
        for (int j = 1; j <= i; j++) {
            cout << caracter;
        }
        cout << endl;
    }
}

int main() {
    int base;
    cout << "Ingrese un número entero positivo: ";
    cin >> base;

    if (base < 1) {
        cout << "El número debe ser positivo." << endl;
        return 1;
    }

    char caracter;
    int opcion;

    cout << "Seleccione una opción (1, 2, 3, o 4): ";
    cin >> opcion;

    switch (opcion) {
        case 1:
            caracter = '*';
            break;
        case 2:
            caracter = '*';
            break;
        case 3:
            caracter = '*';
            break;
        case 4:
            caracter = '*';
            break;
        default:
            cout << "Opción no válida." << endl;
            return 1;
    }

    dibujarTriangulo(base, caracter);

    return 0;
}

python
def dibujarTriangulo(base, caracter):
    for i in range(1, base + 1):
        for j in range(1, i + 1):
            print(caracter, end='')
        print()

def main():
    base = int(input("Ingrese un número entero positivo: "))

    if base < 1:
        print("El número debe ser positivo.")
        return 1

    opcion = int(input("Seleccione una opción (1, 2, 3, o 4): "))

    if opcion not in [1, 2, 3, 4]:
        print("Opción no válida.")
        return 1

    caracter = '*'

    dibujarTriangulo(base, caracter)

if __name__ == "__main__":
    main()
