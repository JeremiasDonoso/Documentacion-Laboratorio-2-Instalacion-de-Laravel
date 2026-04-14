Luego de instalar todo lo requerido para utilizar Laravel pasé directamente a abrir Windows PowerShell y coloqué el comando:

## ![Comando Laravel](https://img.shields.io/badge/1.-composer%20global%20require%20laravel%2Finstaller-6c757d?style=for-the-badge&logo=code&logoColor=white)

La instalación concluyó con dos mensajes, uno en amarillo como si fuera advertencia y uno rojo de error y finalizó el proceso.

## ⚠️ Advertencia 1

[![Advertencia 1](https://raw.githubusercontent.com/JeremiasDonoso/Documentacion-Laboratorio-2-Instalacion-de-Laravel/main/Advertencia%201%20Img.png)](https://raw.githubusercontent.com/JeremiasDonoso/Documentacion-Laboratorio-2-Instalacion-de-Laravel/main/Advertencia%201%20Img.png)

Este problema sucede debido a que la extensión ZIP no ha sido habilitada para PHP, por lo que este no es capaz de descomprimir los archivos necesarios para
la instalación de Laravel. Al darse cuenta que no puede proceder de esta forma, manda la advertencia y busca una alternativa, en este caso intenta descargar
todo desde Git. 
La solución a este primer error es ir a la carpeta donde se ha instalado el PHP, buscar php.ini o php configuration settings y abrirlo utilizando
Visual Studio Code o más sencillo un Bloc de Notas. Al estar dentro del archivo se utiliza Ctrl + F para activar una barra de búsqueda. Se debe colocar aquí
;extension=zip. Al encontrarlo se debe eliminar el ; y guardar el archivo. Ahora sí se podrá instalar Laravel sin problemas.

## ❌ Error 1

```bash
git was not found in your PATH, skipping source download
```
Este sucede debido a que no se tiene instalado Git, por 
lo que no logra completar con éxito la instalación de Laravel y termina el proceso allí mismo. Todo esto se puede evitar al solucionar el primer error, 
pero en caso de no encontrar el ZIP se deberá descargar Git y volver a intentar.

## ![Comando cd](https://img.shields.io/badge/2.-cd%20C%3A%5Cxampp%5Chtdocs-6c757d?style=for-the-badge&logo=code&logoColor=white)

Este comando fue utilizado para cambiar de directorio. Es importante que las carpetas de Laravel se generen aquí debido a que Apache solo puede ver los proyectos
que se encuentren en esa ruta. 

### 3 ▪ 
