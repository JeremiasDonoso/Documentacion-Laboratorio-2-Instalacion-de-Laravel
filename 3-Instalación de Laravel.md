Luego de instalar todo lo requerido para utilizar Laravel pasé directamente a abrir Windows PowerShell y coloqué el comando:

## ![Paso 1](https://img.shields.io/badge/1.-composer%20global%20require%20laravel%2Finstaller-6c757d?style=for-the-badge&logo=code&logoColor=white)

La instalación concluyó con dos mensajes, uno en amarillo como si fuera advertencia y uno rojo de error y finalizó el proceso.

## ⚠️ Advertencia 1

![Advertencia 1](img/Advertencia%201.png)

Este problema sucede debido a que la extensión ZIP no ha sido habilitada para PHP, por lo que este no es capaz de descomprimir los archivos necesarios para
la instalación de Laravel. Al darse cuenta que no puede proceder de esta forma, manda la advertencia y busca una alternativa, en este caso intenta descargar
todo desde Git. 
La solución a este primer error es ir a la carpeta donde se ha instalado el PHP, buscar php.ini o php configuration settings y abrirlo utilizando
Visual Studio Code o más sencillo un Bloc de Notas. Al estar dentro del archivo se utiliza Ctrl + F para activar una barra de búsqueda. Se debe colocar aquí
;extension=zip. Al encontrarlo se debe eliminar el ; y guardar el archivo. Ahora sí se podrá instalar Laravel sin problemas.

## ❌ Error 1

![Error 1](img/Error%201.png)

Este sucede debido a que no se tiene instalado Git, por 
lo que no logra completar con éxito la instalación de Laravel y termina el proceso allí mismo. Todo esto se puede evitar al solucionar el primer error, 
pero en caso de no encontrar el ZIP se deberá descargar Git y volver a intentar.

--- 

## ![Paso 2](https://img.shields.io/badge/2.-cd%20C%3A%5Cxampp%5Chtdocs-6c757d?style=for-the-badge&logo=code&logoColor=white)

Este comando fue utilizado para cambiar de directorio. Es importante que las carpetas de Laravel se generen aquí debido a que Apache solo puede ver los proyectos
que se encuentren en esa ruta. 

---

## ![Paso 3](https://img.shields.io/badge/3.-laravel%20new%20prueba1-6c757d?style=for-the-badge&logo=code&logoColor=white) 

Comando utilizado para crear la primera aplicación Laravel. La primera vez que se utilice saldrán las siguientes preguntas:
## Pregunta 1
![Pregunta 1](img/Pregunta%201%20Laravel.png)

La respuesta NONE fue elegida para utilizar el Laravel básico, sin frontend adicional.

## Pregunta 2
![Pregunta 2](img/Pregunta%202%20Laravel.png)

La herramienta de probado PHPUNIT es la oficial y más usada.

## Pregunta 3
![Pregunta 3](img/Pregunta%203%20Laravel.png)

No veo necesario el uso de IA.

## Pregunta 4
![Pregunta 4](img/Pregunta%204%20Laravel.png)

Estoy usando la base de datos MYSQL, así que esa elegí.

## Pregunta 5
![Pregunta 5](img/Pregunta%205%20Laravel.png)

Necesario para crear las tablas básicas de la nueva base de datos, por eso se debe aceptar.

## ❌ Error 2
![Error 2](img/Error%202%20Laravel.png)

En mi caso no tenía activada la base de datos al momento de intentar la migración, por lo que saltó el error. La solución era simplemente encender la base de datos y volver a intentar migrar.

---

## ![Paso 4](https://img.shields.io/badge/4.-cd%20C%3A%5Cxampp%5Chtdocs%5Cprueba1-6c757d?style=for-the-badge&logo=code&logoColor=white)

Como falló la migración, no se crearon las tablas necesarias para el uso de la base de datos, por lo que es necesario seleccionar la carpeta para manualmente hacer este proceso.

---

## ![Paso 5](https://img.shields.io/badge/5.-php%20artisan%20migrate-6c757d?style=for-the-badge&logo=code&logoColor=white)

Ahora sí se realiza correctamente el proceso de migración.

---

## ![Paso 6](https://img.shields.io/badge/6.-php%20artisan%20serve-6c757d?style=for-the-badge&logo=code&logoColor=white)

Para verificar que el servidor ahora funciona correctamente. Esto es lo que debería de salir en la dirección (http://127.0.0.1:8000):

![comando serve](img/php%20artisan%20serve.png)

---

## ![Paso 7](https://img.shields.io/badge/7.-composer%20require%20laravel%2Fui-6c757d?style=for-the-badge&logo=code&logoColor=white)

Luego de comprobar que todo funciona, este comando se utiliza para instalar el paquete Laravel UI. Este servirá para aplicar una autenticación básica.

---

## ![Paso 8](https://img.shields.io/badge/8.-php%20artisan%20ui%20bootstrap%20--auth-6c757d?style=for-the-badge&logo=code&logoColor=white)

Permite la instalación del bootstrap y crea el sistema de registro e inicio de sesión.

---

## ![Paso 9](https://img.shields.io/badge/9.-npm%20install-6c757d?style=for-the-badge)

Necesario para instalar dependencias que ayudan a la visualización del sistema de inicio de sesión.

## ❌ Error 3
![Error 3](img/Error%203%20Laravel.png)

Sucede porque PowerShell bloquea comandos npm por seguridad. La solución más directa es abrir PowerShell como administrador y utilizar el comando:

![PowerShell](https://img.shields.io/badge/Set--ExecutionPolicy%20RemoteSigned-6c757d?style=for-the-badge&logo=powershell&logoColor=white)

Luego de ejecutar el comando se debe colocar "Y" para aceptar el cambio. Después se debe reiniciar PowerShell y volver a abrirlo. Una alternativa a esto es simplemente usar cmd. 

---

## ![Paso 10](https://img.shields.io/badge/10.-npm%20run%20dev-6c757d?style=for-the-badge)

Usado junto con el comando anterior para compilar el frontend, de forma que se vea ordenado y sea usable por el usuario.

---

## Laravel Instalado

Laravel se ha instalado y se puede utilizar. Sin embargo, al combinar "php artisan serve" y "npm run dev", se genera una nueva vista que no parece terminada. Se puede acceder a la ventana de Inicio de Sesión e incluso es posible crear un usuario y simular un inicio de sesión, pero a partir de aquí la interfaz se pierde. Así se ve al momento de intentar acceder por primera vez: 

![Muestra Laravel](img/MuestraLaravel.png)

---
<div align="center">

### 📌 Información del Laboratorio

🎓 **Universidad Tecnológica de Panamá**

👤 **Estudiante:** Jeremias Donoso  •  📧 **Correo:** jeremias.donoso@utp.ac.pa

📚 **Curso:** Desarrollo de Software 7   •   👩‍🏫 **Instructora:** Irina Fong

📅 **Fecha Final de Ejecución:** 14 de abril de 2026  

---

</div>

