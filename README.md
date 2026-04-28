**Organizacion de computadores**
**Proyecto 2**
2
**2026-1**
**Integrantes proyecto 2**
[Nombre alumno 1]
[Nombre alumno 2]

Punto # 1 - Circuito nuevo: Shifter (25%)
Herramientas a utilizar Aplicacion web de Nand2Tetris
Descripcion El circuito del Shifter tiene la siguiente descripcion en formato HDL:
/*********
* Shifter.hdl - Desplazamiento de un bit a la izquierda o derecha
* Autor 1:
* Autor 2:
*
* Implementacion del siguiente algoritmo:
* if (direction == 0){
* out[0] = 0;
* for(i=2; i < 16; i++)
* out[i] = in[i-1];
* }
* else{
* out[15] = 0;
* for(i=1; i < 15; i++)
* out[i] = in[i-1];
* }
*********/
CHIP Shifter {
IN in[16], // Dato a correr
direction; // Direccion de corrimiento
// 0 = izquierda, 1 = derecha
OUT out[16], // Dato corrido en la direccion solicitada
result; // bit que sale por el extremo
// correspondiente
PARTS:
// Incluya su codigo aqui
}

Un cambio importante respecto circuito visto en clase es que esta especificacion
tiene un campo result, por el cual sale el bit que fue empujado en el extremo
correspondiente. Para entender esto, mire la siguiente tabla:
Entrada
direction
Entrada in[16]
(ejemplo)
Salida out[16]
(esperada)
Salida
result
0 1000 0000 0000 0001 0000 0000 0000 0010 1
1 1000 0000 0000 0001 0100 0000 0000 0000 1
Tabla 1. Casos de prueba propuestos

En el caso donde direction es 0, el bit 15 (el mas significativo) se lleva a result
(por eso esta en 1) y en el bit 0 aparece un 0. Lo inverso pasa cuando el bit
direction es 1 (sale en result el bit 0 que estaba en 1 y en el bit 15 aparece un 0.
El resto del numero se corre un bit en la direccion indicada por direction.
Implementar en HDL el circuito que resuelve el shifter tanto a la izquierda como
a la derecha.
Condiciones a validar Use los casos de prueba mostrados en la tabla 1 para
validar que el circuito funciona correctamente.
Entregables Subir a su repositorio de GIT en la carpeta proyecto2 los siguientes
archivos:
1. Shifter.hdl con el circuito del Shifter.
2. Crear un archivo llamado Shifter.md5 con la salida de la siguiente pagina
web donde debe subir el archivo una vez este listo:
https://emn178.github.io/online-tools/md5_checksum.html
