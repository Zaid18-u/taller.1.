#include <stdio.h>

int main() {
    int id, stock, cantidad, opcion;
    float precio, total_ganancias = 0, venta = 0, descuento = 0;
    char nombre[30];
    int check;

    do {
        printf("\nMenu de Opciones:\n");
        printf("1. Registrar producto\n");
        printf("2. Vender producto\n");
        printf("3. Reabastecer producto\n");
        printf("4. Mostrar informacion del producto\n");
        printf("5. Mostrar total de ganancias\n");
        printf("6. Salir\n");
        printf("Seleccione una opcion: ");
        scanf("%d", &opcion);

        switch(opcion) {

            case 1:
                do{
                do{
                printf("Ingrese el ID del producto: ");
                check = scanf("%d", &id);
                if(check != 1){
                    printf("Cantidad de stock no valida.");
                }
                }while (check != 1);

                printf("Ingrese el nombre del producto: ");
                fflush(stdin);
                fgets(nombre, 30, stdin);
                
                do{
                printf("Ingrese la cantidad inicial en stock: ");
                fflush(stdin);
                check = scanf("%d", &stock);
                if(check != 1){
                    printf("Cantidad de stock no valida.\n");
                }
                }while (check != 1);
                do {
                printf("Ingrese el precio unitario del producto: ");
                fflush(stdin);
                check = scanf("%f", &precio);
                if(check != 1){
                    printf("Precio no valido.\n");
                }
                }while (check != 1);

                if(stock < 1){
                    printf("Cantidad de stock no valida.\n");
                }
                if(precio <= 0){
                    printf("Precio no valido.\n");
                }

                }while (stock < 1 || precio <= 0);

                break;

            case 2:
                do
                {
                    do{
                    printf("Ingrese la cantidad a vender: ");
                    fflush(stdin);
                    check = scanf("%d", &cantidad);
                    if(check != 1){
                        printf("Cantidad no valida.");
                    }
                    }while (check != 1);
                    if (cantidad < 1)
                    {
                        printf("el numero ingresado no es correcto\n");
                    }
                    if (cantidad > stock)
                    {
                        printf("No existe suficiente producto para esta venta, vuelva a ingresar\n");
                    }

                } while (cantidad < 1 || cantidad > stock);
                venta = cantidad * precio;
                if(cantidad > 20){
                    descuento = venta * 0.20;
                    venta -= descuento;
                }
                stock -= cantidad;
                total_ganancias += venta;

                break;

            case 3:
                do
                {
                    do{
                    printf("Ingrese la cantidad a agregar al stock: ");
                    check = scanf("%d", &cantidad);
                    if(check != 1){
                        printf("Cantidad no valida.");
                    }
                    }while (check != 1);

                    if (cantidad < 1)
                    {
                        printf("el numero ingresado no es correcto\n");
                    }
                } while (cantidad < 1);
                stock += cantidad;

                break;

            case 4:
                printf("\nInformación del producto:\n");
                printf("ID: %d\n", id);
                printf("Nombre: %s", nombre);
                printf("Stock disponible: %d\n", stock);
                printf("Precio unitario: %.2f\n", precio);

                break;

            case 5:
                printf("Total de ganancias: $%.2f\n", total_ganancias);

                break;

            case 6:
                printf("Saliendo del programa...\n");

                break;

            default:
                printf("Opcion invalida. Intente nuevamente.\n");
        }
    } while (opcion != 6);

    return 0;
}
