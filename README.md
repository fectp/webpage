# webpage
Sitio Web de la FECTP

## Imágenes

Para incrustar imágenes por favor siga las [instrucciones de Ayush Sharma](https://opensource.com/article/21/12/optimize-web-images-linux).

Copie las imágenes y aplique el tamaño adecuado, en este caso para la página principal es 540x406

  mogrify -resize 540x406 *.png
  mogrify -format jpg -resize 540x406 *.jpg

Para optimizar

  for i in *.png; do optipng -o5 -quiet "$i"; done
  jpegoptim -sq *.jpg


## Para uso diario

  hugo serve

## Prepublicación

  rm -rf public/*
  hugo

En otra ventana ejecutar desde el directorio `public`

  python3 -m http.server

Y visitar con el navegador http://localhost:8000 o el puerto que haya sido asignado por el servidor web que ofrece Python.


