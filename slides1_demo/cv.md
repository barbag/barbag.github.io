---
title:  'Presentación Epubs'
date: '7 de marzo de 2023'
author:
- Cristina Fernández Fernández
classoption:
- aspectratio=169
---
# Epubs

## Introducción

* ¿Qué es un **Epub**?
	
	- Formato de archivo de libro electrónico.
	
	- Extensión .epub.
	
	- Es un estándar publicado por el International Digital Publishing Forum (IDPF).
	
	- Sustituye al antiguo estándar Open eBook.
	
	- Nació en octubre de 2007.

## ¿Cómo está construido?

* Especificaciones

	- _Open Publication Structura_ (OPS) 2.0.1, comprende el formato de su contenido. [Más información](https://idpf.org/epub/20/spec/OPS_2.0.1_draft.htm)
	
	- _Open Packaging Format_ (OPF) 2.0.1, describe la estructura del archivo .epub en XML. [Más información](https://idpf.org/epub/20/spec/OPF_2.0_final_spec.html)
	
	- _Open Container Format_ (OCF) 2.0.1, agrupa todos los archivos como un archivo ZIP. [Más información](https://idpf.org/epub/30/spec/epub30-ocf-20111011.html)

* Ejemplo de OPF
```html
<?xml version="1.0"?>
<package version="2.0" xmlns="http://www.idpf.org/2007/opf" unique-identifier="BookId">

  <metadata xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:opf="http://www.idpf.org/2007/opf">
    <dc:title>Pride and Prejudice</dc:title>
    <dc:language>en</dc:language>
    <dc:identifier id="BookId" opf:scheme="ISBN">123456789X</dc:identifier>
    <dc:creator opf:file-as="Austen, Jane" opf:role="aut">Jane Austen</dc:creator>
  </metadata>

  <manifest>
    <item id="chapter1" href="chapter1.xhtml" media-type="application/xhtml+xml"/>
    <item id="appendix" href="appendix.xhtml" media-type="application/xhtml+xml"/>
    <item id="stylesheet" href="style.css" media-type="text/css"/>
    <item id="ch1-pic" href="ch1-pic.png" media-type="image/png"/>
    <item id="myfont" href="css/myfont.otf" media-type="application/x-font-opentype"/>
    <item id="ncx" href="toc.ncx" media-type="application/x-dtbncx+xml"/>
  </manifest>

  <spine toc="ncx">
    <itemref idref="chapter1" />
    <itemref idref="appendix" />
  </spine>

  <guide>
    <reference type="loi" title="List Of Illustrations" href="appendix.xhtml#figures" />
  </guide>

</package>
```
	
## Ejemplos de Epub

![Ejemplo Epub](Imagenes/epubs.png)


## Ejemplo de estructura XHTML para un Epub

```html
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
  <head>
    <meta http-equiv="Content-Type" content="application/xhtml+xml; charset=utf-8" />
    <title>La sombra del ciprés es alargada</title>
    <link rel="stylesheet" href="css/main.css" type="text/css" />
  </head>
  <body>
    ...
  </body>
</html>
```
## ¿Por qué usar Epub?
[¿Qué es EPUB y por qué deberías empezar a usarlo?](https://www.youtube.com/watch?v=P1ps5p57GSk&ab_channel=ericsoloconc)

