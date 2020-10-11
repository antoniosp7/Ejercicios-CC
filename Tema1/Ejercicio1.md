# Ejercicios de autoevaluación Tema 1

## Ejercicio 1

La aplicación elegida es la realizada en una asignatura cursada llamada Inteligencia Artificial, esta aplicación resolvía el enigma lógico Hitori.

El patrón usado es una arquitectura en capas, donde se puede apreciar una capa presentación formada por los usuarios que querían resolver un nuevo enigma Hitori, una capa de lógica de negocio escrita en el lenguaje Python y una capa de datos formada por una base de datos SQLite.

Si se quisiera ascender a una arquitectura microservicios tendríamos que desplegar tanto la capa de lógica de negocio como la capa de datos de forma independiente e incluir un sistema de gestión de eventos entre los servidores el cual recoja las llamadas de la capa de lógica de negocio y las sirva a la capa de datos.

