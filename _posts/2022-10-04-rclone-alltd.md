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

``` curl https://rclone.org/install.sh | sudo bash```

## Paso 2
Como estoy usand Windows tan solo descargo el .zip y lo descomprimo, el resultado sera una carpeta con este contenido:

![paso2.img1](https://telegra.ph/file/fab62f672ad86cb08ea83.png){: .mx-auto.d-block :}

## Paso 3

Dejamos solo el archivo rclone.exe y borramos el resto, ahora creamos un archivo de texto con el nombre rclone, y le cambiamos la extension a .conf. El resultado final debería quedar así:

![paso3.img1](https://telegra.ph/file/9abba51d48dcd039632b9.png){: .mx-auto.d-block :}

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
