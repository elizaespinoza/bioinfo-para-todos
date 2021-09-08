[![CC BY 4.0][cc-by-shield]][cc-by]

# Acceso remoto al servidor

Vamos a realizar la parte práctica de este curso en el servidor de Bioinfo de la UFMG. De acuerdo al SO de tu computador, sigue las instrucciones a seguir:

## *Windows*

1. Instala el programa PuTTy ([32 bits](https://the.earth.li/~sgtatham/putty/latest/w32/putty.exe) o [64 bits](https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe)) en tu computador.

> *PuTTy permite realizar conexiones SSH para conseguir entrar, acceder, modificar y administrar a un servidor de forma remota.*

2. Abre el programa y coloca (o escoge) los siguientes datos:
    * Host name (or IP address): <code>150.164.23.203</code>
    * Port: <code>22</code>
    * Conection type: <code>SSH</code>
    * Close Window on exit: <code>Only on clean exit</code>

3. Clica en <code>Save</code> para guardar la sesión con el nombre <code>tbioinfo</code>.
4. Clica en <code>Open</code>.

> *Cuando quieras ingresar de nuevo solo clica en <code>tbioinfo</code> y el terminal abrirá para que entres al servidor luego de colocar el usuario y la contraseña.*

5. Inicia sesión digitando <code>trujillo</code> y da enter.
6. Ahora digita la contraseña que pasaremos en la reunión síncrona.

## *Linux*

1. (En Ubuntu) Abre tu terminal escribiendo <code>[ctrl+alt+T]</code>.
2. Digita el comando <code>ssh trujillo@150.164.23.203</code> para entrar al servidor.
3. Digita la contraseña.

¡Genial! Ya entramos en el servidor. Estamos listos para comenzar la [**parte práctica**](../a1-bashLinux.md#1-practica).

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg