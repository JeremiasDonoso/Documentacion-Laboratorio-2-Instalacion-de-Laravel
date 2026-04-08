Luego de instalar todo lo requerido para utilizar Laravel pasé directamente a abrir Windows PowerShell y coloqué el comando:
1 ▪ composer global require laravel/installer

La instalación concluyó con un mensaje en color Amarillo (Imagen Advertencia Zip) y un mensaje en color Rojo (Imagen Error Git).
La advertencia en amarillo dice: "Failed to download laravel/installer from dist: The zip extension and unzip/7z commands are both missing, skipping.
The php.ini used by your command-line PHP is: C:\xampp\php\php.ini
    Now trying to download from source"
Este problema sucede debido a que la extensión ZIP no ha sido habilitada para PHP, por lo que este no es capaz de descomprimir los archivos necesarios para
la instalación de Laravel. Al darse cuenta que no puede proceder de esta forma, manda la advertencia y busca una alternativa, en este caso intenta descargar
todo desde Git. 
La solución a este primer error es ir a la carpeta donde se ha instalado el PHP, buscar php.ini o php configuration settings y abrirlo utilizando
Visual Studio Code o más sencillo un Bloc de Notas. Al estar dentro del archivo se utiliza Ctrl + F para activar una barra de búsqueda. Se debe colocar aquí
;extension=zip. Al encontrarlo se debe eliminar el ; y guardar el archivo. Ahora sí se podrá instalar Laravel sin problemas.

El segundo error dice:  "git was not found in your PATH, skipping source download". Este sucede debido a que no se tiene instalado Git, por 
lo que no logra completar con éxito la instalación de Laravel y termina el proceso allí mismo. Todo esto se puede evitar al solucionar el primer error, 
pero en caso de no encontrar el ZIP se deberá descargar Git y volver a intentar.


2 ▪ cd C:\xampp\htdocs
Este comando fue utilizado para cambiar de directorio. Es importante que las carpetas de Laravel se generen aquí debido a que Apache solo puede ver los proyectos
que se encuentren en esa ruta. 

3 ▪ 
