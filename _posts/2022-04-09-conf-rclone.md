---
layout: post
title: Configurar rclone
subtitle: Utilizar rclone con Google Drive
tags: [tutorial]
comments: false
---

En este tutorial aprenderas a realizar una configuración básica de rclone con Google Drive, pero lo puedes aplicar a cualquiero otra nube soportada por el programa

## Paso 1

Lo primero que deberemos hacer sera descargar rclone desde su web oficial: [Descargar rclone](https://rclone.org/downloads/) - en el caso de que tu sistema sea Linux/macOS/BSD solo deberas ejecutar el siguiente comando en la consola: 

~~~ 
curl https://rclone.org/install.sh | sudo bash 
~~~

## Paso 2

Una vez instalado el programa ejecutamos el comando _rclone config_ como se ve en la siguiente imagen:

![image](https://user-images.githubusercontent.com/115044134/195947126-22b10f23-e8ab-4236-84b8-1d3e07ce546f.png){: .mx-auto.d-block :}

## Paso 3

Ahora ingresamos la letra _n_ en el teclado para crear un nuevo "remoto" e ingresamos el nombre que queremos asignarle, en este caso le asigne el nombre gdrive pero puedes colocar lo que quieras.

![image](https://user-images.githubusercontent.com/115044134/195947190-b4b8fc8a-0b2e-4b6e-8302-9b241ec79788.png){: .mx-auto.d-block :}

## Paso 4

Presionamos la tecla enter y nos aparece una pantalla como la siguiente:

![image](https://user-images.githubusercontent.com/115044134/195947221-4bfb51f1-9406-47e2-abe4-15983608e20e.png){: .mx-auto.d-block :}

Aqui escrbimos la palabra drive para configurar nuestra cuenta o Unidad Compartida de Google Drive.

## Paso 5

Luego de eso nos apareceran las siguientes opciones:

![image](https://user-images.githubusercontent.com/115044134/195947265-cfea7571-d3b4-44b1-a8d7-276dc26152f3.png){: .mx-auto.d-block :}

**Es mejor que configures tu propio client_id y secret ya que las genéricas se comparten entre cientos de usuarios** pero para no alargar el tutorial eso no lo explicare aqui, asi que presionamos le tecla enter y en la siguiente opción la presionamos nuevamente. PASOS PARA CREAR TU ID Y SECRET: [click aquí](https://rclone.org/drive/#making-your-own-client-id)

## Paso 6

En la siguiente pantalla digitamos el número 1 tal y como se muestra:

![image](https://user-images.githubusercontent.com/115044134/195947333-30a54df9-ccac-4ba5-ad1e-7470c7d5a545.png){: .mx-auto.d-block :}

## Paso 7

Ahora presionamos la tecla _enter_ en las siguientes opciones, cambialas solo si sabes lo que haces.

![image](https://user-images.githubusercontent.com/115044134/195947385-d1561dd5-f7fd-4f90-8f30-314fe5734aa3.png){: .mx-auto.d-block :}

## Paso 8

En la siguiente opción tendremos que digitar la letra "n" porque estamos configurandolo en un dispositivo al que solo podemos acceder mediante linea de comandos, luego de eso presionamos la tecla _enter_.

![image](https://user-images.githubusercontent.com/115044134/195947435-70bbb1f2-8d1a-42f2-8edd-8ead65b576eb.png){: .mx-auto.d-block :}

Lo anterior nos dara como resultado lo siguiente:

![image](https://user-images.githubusercontent.com/115044134/195947456-fcaef610-96b9-40f3-be5a-8266cb5a8e76.png){: .mx-auto.d-block :}

## Paso 9

Tendremos que copiar lo que esta subrayado en rojo, descargamos rclone en alguna PC que cuente con un navegador, en mi caso utilizare una computadora con Windows 10 asi que descargo la versión de rclone para dicho sistema [(ver paso 1)](#paso-1), descargamos y descomprimimos el archivo .zip dandonos como resultado los siguientes archivos:

![image](https://user-images.githubusercontent.com/115044134/195947091-f20cef59-11d1-4818-84be-05f94fb1fd5b.png){: .mx-auto.d-block :}

Ahora tendremos que abrir la consola en dicha carpeta, para ello escribimos las letras "cmd" en la barra superior donde aparece la ruta de la carpeta, y presionamos la tecla _enter_ tal y como se muestra en la siguiente imagen

![image](https://user-images.githubusercontent.com/115044134/195947060-2754af16-0457-4111-b693-5385fc886390.png){: .mx-auto.d-block :}

Lo anterior abrirá la consola de comandos donde tendremos que pegar el comando que copiamos anteriormente del [paso 8](#paso-8), y presionamos la tecla _enter_.

![image](https://user-images.githubusercontent.com/115044134/195947029-92a9650f-bf97-4aa4-a130-37fbea7feacd.png){: .mx-auto.d-block :}

Esto nos abrirá el navegador para inicar sesión, allí iniciaremos sesión con el correo de Google Drive que queremos configurar en rclone.

## Paso 10

Una vez iniciada sesión, en la consola nos aparecerá un código como el siguiente:

![image](https://user-images.githubusercontent.com/115044134/195947613-267695d1-407a-4c15-a4a2-fe89e7313ed5.png){: .mx-auto.d-block :}

Copiamos dicho código y lo pegamos en la consola de servidor donde nos estaba pidiendo el config_token como se muestra en la siguiente imagen:

![image](https://user-images.githubusercontent.com/115044134/195947628-5c04663b-4b80-493b-bd4e-0a7d5a398642.png){: .mx-auto.d-block :}

## Paso 11

Ahora el programa nos esta preguntando si queremos configurar el remoto como una Unidad Compartida, en este caso yo presionare la tecla _y_ ya que si lo quiero configurar como una Unidad Compartida, si quieres usar tu unidad raiz entonces introduce la letra _n_ y presionas enter.

![image](https://user-images.githubusercontent.com/115044134/195947788-5df1d900-5d17-47fe-a4a4-ddbd9a72b122.png){: .mx-auto.d-block :}

Ahora nos aparecerá un listado con todas las Unidades Compartidas a las que somos miembros, buscamos la que queremos configurar y escrbimos el número que corresponde a la unidad (dicho número se encuentra a la izquierda del todo).

Luego de esto nos aparecera la siguiente información preguntándonos si la información es correcta, presionamos la tecla _y_ y luego la tecla _enter_.

![image](https://user-images.githubusercontent.com/115044134/195947996-e648f411-1e9c-4f9e-8be0-70781c7a0b30.png){: .mx-auto.d-block :}

Nos aparecerá nuevamente la información del [paso 3](#paso-3) donde esta vez presionaremos la tecla _q_ seguido de la tecla enter para salirnos de rclone.

Ahora ya puedes montar tu unidad de rclone de la forma en que gustes

## Tutorial creado por [@mau671](https://t.me/mau671)
