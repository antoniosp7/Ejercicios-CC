# Ejercicio 4 Examinar la estructura de capas que se forma al crear imágenes nuevas a partir de contenedores que se hayan estado ejecutando

Una vez tengamos el sha256 del commit podemos proceder a ver el json asociado con el siguiente comando en nuestro caso.

    sudo jq '.' /var/lib/docker/image/overlay2/imagedb/content/sha256/6cc5e67c72d5d84beab58f502d54b16303eba8187a46a7c9a801813e6e7ba783^C

Aquí podemos ver el resultado de ejecutar este comando.

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/dockercommitjson.png)