# Ejercicio 2

El primer paso será crear los dockerfile, para ello hemos seguido las directrices de la siguiente [página](https://examples.javacodegeeks.com/devops/docker/docker-hello-world-example/).

Clase HelloWorld : 

    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello, World");
        }
    }

## Fedora
  
Este sería el dockerfile correspondiente para Fedora, en el cual añadimos la clase HelloWorld mostrada anteriormente, a su vez se instala openjdk8 con el comando válido para Fedora y CentOS yuml.

    FROM fedora:latest
    
    LABEL maintainer="antoniosalvatperez@gmail.com"
    
    ADD HelloWorld.class HelloWorld.class

    RUN yum install -y \
        java-1.8.0-openjdk \
        java-1.8.0-openjdk-devel

    ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "HelloWorld"]

Aquí mostramos la build de docker y como se ejecutaría.

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/dockerBuildFedora.png)

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/dockerRunAlpine.png)
 

## CentOS

Este sería el dockerfile correspondiente para CentOS, en el cual añadimos la clase HelloWorld mostrada anteriormente, a su vez se instala openjdk8 con el comando válido para Fedora y CentOS yuml.

    FROM centos:latest
    
    LABEL maintainer="antoniosalvatperez@gmail.com"
    
    ADD HelloWorld.class HelloWorld.class

    RUN yum install -y \
        java-1.8.0-openjdk \
        java-1.8.0-openjdk-devel

    ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "HelloWorld"]

Aquí mostramos la build de docker y como se ejecutaría.

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/dockerBuildCentos.png)

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/dockerRunCentos.png)
 

## Alpine

Este sería el dockerfile correspondiente para Alpine, en el cual añadimos la clase HelloWorld mostrada anteriormente, a su vez se instala openjdk8 con el comando válido para Alpine apk yuml.


    FROM alpine:latest
 
    LABEL maintainer="antoniosalvatperez@gmail.com"
 
    ADD HelloWorld.class HelloWorld.class

    RUN apk --update add openjdk8-jre

    ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "HelloWorld"]

Aquí mostramos la build de docker y como se ejecutaría.

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/dockerBuildAlpine.png)

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/dockerRunAlpine.png)



## Comparación 

Aquí podemos ver la comparación del peso del programa Hello World en los distintos sistemas, el primero se correspondería con Cent0S, el segundo con Fedora y el tercero con Apine.

![](https://raw.githubusercontent.com/antoniosp7/Ejercicios-CC/main/Tema3/images/DockerImages.png)
 


