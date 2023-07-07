#include <stdio.h>
#include <string.h>

#define PRODUCTOS 5

// Estructura para representar un dulce mexicano
struct DulceMexicano {
    char nombre[50];
    float valor;
    int inventario;
};

// Inventario inicial de los dulces mexicanos
struct DulceMexicano inventario[PRODUCTOS] = {
    {"Dulce 1", 10.0, 10},
    {"Dulce 2", 15.0, 5},
    {"Dulce 3", 12.5, 8},
    {"Dulce 4", 8.0, 15},
    {"Dulce 5", 9.5, 20}
};

float dineroDisponible = 0.0;
int ventasRealizadas = 0;

// Función para despachar un producto y entregar cambio
void despacharProducto(int producto, float pago) {
    if (producto >= 1 && producto <= PRODUCTOS) {
        if (inventario[producto - 1].inventario > 0) {
            if (pago >= inventario[producto - 1].valor) {
                printf("Despachando producto: %s\n", inventario[producto - 1].nombre);
                inventario[producto - 1].inventario--;

                // Calcular y entregar cambio
                float cambio = pago - inventario[producto - 1].valor;
                printf("Entregando cambio: $%.2f\n", cambio);

                // Actualizar dinero disponible y ventas realizadas
                dineroDisponible += inventario[producto - 1].valor;
                ventasRealizadas++;
            } else {
                printf("Pago insuficiente. Se requiere un pago mínimo de $%.2f\n", inventario[producto - 1].valor);
            }
        } else {
            printf("Producto agotado. Informar al administrador.\n");
        }
    } else {
        printf("Producto inválido\n");
    }
}

int main() {
    int i;
    int admin = 0;

    printf("---- MÁQUINA EXPENDEDORA ----\n");

    printf("\n---- MENÚ DE VENTAS ----\n");
    printf("Productos disponibles:\n");
    for (i = 0; i < PRODUCTOS; i++) {
        printf("%d. %s - $%.2f\n", i + 1, inventario[i].nombre, inventario[i].valor);
    }

    while (1) {
        int producto;
        float pago;

        printf("\nIngrese el número del producto (1-%d) o ingrese 0 para salir: ", PRODUCTOS);
        scanf("%d", &producto);

        if (producto == 0) {
            printf("¡Gracias por utilizar la máquina expendedora!\n");
            break;
        }

        printf("Ingrese el pago: $");
        scanf("%f", &pago);

        despacharProducto(producto, pago);
    }

    while (1) {
        printf("\nIngrese la contraseña de administrador (0 para salir): ");
        scanf("%d", &admin);

        if (admin == 1234) {
            printf("\n---- MENÚ DE ADMINISTRADOR ----\n");

            // Estadísticas del administrador
            printf("\nResumen del administrador:");
            printf("\n- Dinero disponible: $%.2f", dineroDisponible);
            printf("\n- Ventas realizadas: %d\n", ventasRealizadas);

            break;
        } else if (admin == 0) {
            printf("¡Gracias por utilizar la máquina expendedora!\n");
            return 0;
        } else {
            printf("Contraseña incorrecta. Inténtelo nuevamente.\n");
        }
    }

    return 0;
}
