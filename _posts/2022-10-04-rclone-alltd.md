---
layout: post
title: Montar multiples TD con rclone
subtitle: Aplicable a cualquier OS
#gh-repo: daattali/beautiful-jekyll
#gh-badge: [star, fork, follow]
tags: [tutorial]
comments: false
---

En este tutorial aprenderas a montar todas las TD de una misma cuenta de una forma sencilla sin tener que montar cada unidad por separado.

## Paso 1

Lo primero que deberemos hacer sera descargar rclone desde su web oficial: [Descargar rclone](https://rclone.org/downloads/) - en el caso de que tu sistema sea Linux/macOS/BSD solo deberas ejecutar el siguiente comando en la consola: 

~~~ 
curl https://rclone.org/install.sh | sudo bash 
~~~

## Paso 2
Como estoy usand Windows tan solo descargo el .zip y lo descomprimo, el resultado sera una carpeta con este contenido:

![paso2.img1](https://telegra.ph/file/fab62f672ad86cb08ea83.png){: .mx-auto.d-block :}

## Paso 3

Dejamos solo el archivo rclone.exe y borramos el resto, ahora creamos un archivo de texto con el nombre rclone, y le cambiamos la extension a .conf. El resultado final debería quedar así:

![paso3.img1](https://telegra.ph/file/9abba51d48dcd039632b9.png){: .mx-auto.d-block :}

Ahora escribimos _rclone config_ y en el menu que nos aparece presionas la tecla _n_ y luego enter

![paso3.img2](https://telegra.ph/file/0f9b377279f2c0ca0c9db.png){: .mx-auto.d-block :}

## Paso 4

Aqui escribimos un nombre para la unidad, en este caso le colocare drive pero puedes colocar cualquier nombre

![paso4.img1](https://telegra.ph/file/237352e5890dd1d40ccef.png){: .mx-auto.d-block :}

Ahora en esta lista que nos aparece escribimos la palabra _drive_ para usar Google Drive

![paso4.img2](https://telegra.ph/file/aa66921f0b047057e090d.png){: .mx-auto.d-block :}

En todas estas opciones presionamos solo enter a no ser que quieras cambiar alguna cosa como el client id y client secret por unos tuyos: [Más info](https://rclone.org/drive/#making-your-own-client-id)

![paso4.img3](https://telegra.ph/file/0ccc64812ce473722f6cb.png){: .mx-auto.d-block :}

![paso4.img4](https://telegra.ph/file/8edea82b6c6c11effbb42.png){: .mx-auto.d-block :}

Lo anterior nos abrirá el sitio web para iniciar sesión con nuestra cuenta de Google, una vez iniciada la sesión volvemos a la consola, nos aparecerá una opción para configurarlo como Unidad Compartida, presionaremos la tecla _n_ y luego enter

![paso4.img5](https://telegra.ph/file/9c0bd2787ed86fb22e2eb.png){: .mx-auto.d-block :}

Verificamos que toda la información este correcta y presionamos la tecla _y_

![paso4.img6](https://telegra.ph/file/04164ed329aeed956fec2.png){: .mx-auto.d-block :}

Y ahora salimos de rclone con la tecla _q_

![paso4.img6](https://telegra.ph/file/542c78dbd8f531911753a.png){: .mx-auto.d-block :}

## Paso 5

Ahora ejecutamos el siguiente comando:

~~~
rclone backend -o config drives drive:
~~~

{: .box-note}
**Nota:** cambiar drive: por el nombre que le colocaste al remoto en el [paso 4](#paso-4), por ejemplo, si le colocaste pepito el comando cambiaria a _rclone backend -o config drives pepito:_

Ese comando nos generará algo similar a lo siguiente en la consola: 

![paso5.img1](https://telegra.ph/file/f649842083e8d8d47c7da.png){: .mx-auto.d-block :} 

## Paso 6

Copiamos todo el resultado del comando anterior y lo pegamos en el archivo rclone.conf que creamos en el [paso 2](#paso-4), el archivo ahora deberia lucir de la siguiente manera:

![paso6.img1](https://telegra.ph/file/72a6817b8e1a4889555f6.png){: .mx-auto.d-block :} 

{: .box-note}
**Nota:** Tambien agregar _server_side_across_configs = true_ en el primer remoto para poder mover entre unidades sin descargar y volver a subir y asi poder renombrar archivos con FileBot o TMM entre distintas unidades, el archivo debería verse así:

![paso6.img2](https://telegra.ph/file/3198e705e9aebf79b0e12.png){: .mx-auto.d-block :} 

## Paso 7
Ahora guardamos el archivo y montamos la unidad llamada AllDrives, puedes personalizar el comando a tu gusto, agregando cache y otras opciones. Yo utilizare algo basico el cual es el siguiente comando: 

~~~
rclone mount AllDrives: *
~~~

El resultado deberia ser similar a lo siguiente:

![paso7.img1](https://telegra.ph/file/1e8cf0c681ef342531df7.png){: .mx-auto.d-block :} 

{: .box-error}
**Advertencia:** Si el comando anterior falla tienes que instalar el programa WinFsp desde el siguiente enlace: https://winfsp.dev/rel/ y ejecutar el comando nuevamente

Ahora podremos ver que todas las unidades compartidas de la cuenta se montaron en una misma unidad de Windows (o carpeta en Linux)

![paso7.img2](https://telegra.ph/file/e4929e36b1f3afe0694b6.png){: .mx-auto.d-block :} 

{: .box-warning}
Para que la unidad quede montada e inicie automáticamente con el sistema en Windows se debe usar nssm, tutorial [aqui](https://blog.storagemadeeasy.com/running-windows-rclone-mount-as-a-service/) 

## Tutorial creado por [@mau671](https://t.me/mau671)
