MÁQUINA EXPENDEDORA - README

Este programa simula el funcionamiento de una máquina expendedora de dulces mexicanos. Permite a los usuarios seleccionar productos, realizar pagos y recibir el producto y el cambio correspondiente.

INSTRUCCIONES DE USO:

1. Compilación del programa:
   - Asegúrate de tener un compilador de C instalado en tu sistema.
   - Abre una terminal y navega hasta el directorio donde se encuentra el archivo del programa (vending_machine.c).
   - Compila el programa usando el comando de compilación adecuado. Por ejemplo, si estás utilizando el compilador de GCC, ejecuta el siguiente comando:
     ```
     gcc -o vending_machine vending_machine.c
     ```

2. Ejecución del programa:
   - Una vez compilado, ejecuta el programa con el siguiente comando:
     ```
     ./vending_machine
     ```

3. Menú de ventas:
   - En el menú de ventas, verás una lista de productos disponibles junto con sus nombres y precios.
   - Ingresa el número del producto que deseas comprar y luego ingresa el monto de pago.
   - El programa despachará el producto seleccionado y entregará el cambio si corresponde.

4. Menú de administrador:
   - Para acceder al menú de administrador, se requiere una contraseña de administrador.
   - Ingresa la contraseña de administrador cuando se solicite (por defecto, la contraseña es 1234).
   - En el menú de administrador, se mostrarán estadísticas relacionadas con el dinero disponible y las ventas realizadas.

5. Salida del programa:
   - Para salir del programa en cualquier momento, ingresa 0 en lugar de seleccionar un producto o ingresar una contraseña.

NOTAS ADICIONALES:

- Puedes ajustar la configuración de los productos y su inventario modificando el arreglo 'inventario' en el archivo vending_machine.c.
- Si deseas cambiar la contraseña de administrador, modifica la variable 'admin' en el archivo vending_machine.c.

¡Disfruta utilizando la máquina expendedora de dulces mexicanos!

