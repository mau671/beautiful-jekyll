---
layout: post
title: Montar varias TD (misma cuenta) con rclone
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

Ahora escribimos _rclone config_ y en el menu que nos aparece presionas la letra n y luego enter

![paso3.img2](https://telegra.ph/file/0f9b377279f2c0ca0c9db.png){: .mx-auto.d-block :}

## Paso 4

Aqui escribimos un nombre para la unidad, en este caso le colocare drive pero puedes colocar cualquier nombre

![paso4.img1](https://telegra.ph/file/237352e5890dd1d40ccef.png){: .mx-auto.d-block :}

Ahora en esta lista que nos aparece escribimos la palabra _drive_ para usar Google Drive

![paso4.img2](https://telegra.ph/file/aa66921f0b047057e090d.png){: .mx-auto.d-block :}

En todas estas opciones presionamos solo enter a no ser que quieras cambiar alguna cosa como el client id y client secret por unos tuyos: [Más info](https://rclone.org/drive/#making-your-own-client-id)

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.
