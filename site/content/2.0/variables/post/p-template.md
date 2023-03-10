---
title: p.template
weight: 5
pro_heading: "full, centered, fixed,  featured, product, Combinaciones"
---

Establece la **plantilla de entradas** predeterminada, la cual configura la estructura del articulo para brindarle nuevas características que de otra manera, no serian accesibles. Este valor se puede [sobrescribir en las entradas individuales]({{< ref "templates.md" >}}).

```html
<Variable name="p.template" description="Default post template" type="string" value="default"/>
```

## Valores disponibles

Si el valor ingresado no es válido, el valor por defecto será `default`.

{{< table >}}
| Value          | Nombre             | Tipo                 | Descripción
| -------------- | ------------------ | -------------------- | --------------
| `default`      | Por defecto        | {{< data string >}}  | Estructura común de articulo
| `hero`         | Header hero        | {{< data string >}}  | Modo header hero
| `full`         | Full               | {{< data string >}}  | Modo ancho completo sin sidebar
| `centered`     | Contenido centrado | {{< data string >}}  | Modo contenido centrado sin sidebar
| `fixed`        | Fondo fijo         | {{< data string >}}  | Modo fondo de imagen principal fijo
| `featured`     | Imagen destacada   | {{< data string >}}  | Modo imagen principal destacada
| `product`      | Producto           | {{< data string >}}  | Modo producto de tienda
{{< /table >}}

## default

Diseño predeterminado del artículo, este valor se utiliza también por defecto si la plantilla especificada **no existe** o si el valor ingresado es **inválido**.

{{< pagelink title="Demostración Default" name="Maily" href="https://maily.zkreations.com/2022/12/castle-in-corfu-greece.html" >}}


## hero

Muestra una nueva cabecera en el articulo, comúnmente conocida como "header hero". Los metadatos y el título de la entrada se trasladan a este nuevo header.

{{< pagelink title="Demostración Hero" name="Maily" href="https://maily.zkreations.com/2023/01/wooden-bridge-near-forest.html" >}}


## full

La plantilla elimina el sidebar y la entrada se extiende hasta ocupar **todo el ancho disponible**. Este valor tendrá prioridad sobre la variable [f.sidebarIn]({{< ref "f-sidebar-in.md" >}}).


## centered

Similar al modo ancho completo, pero también centra el contenido en relación al cuerpo de la entrada.


## fixed

Utiliza la primera imagen disponible en el articulo y la muestra de fondo manteniendo una posición fija.

## featured

Destaca la imagen principal de la entrada mostrando los metadatos y el título en su interior. Este modo posiciona la imagen antes que las etiquetas.


{{< pagelink title="Demostración Featured" name="Maily" href="https://maily.zkreations.com/2022/12/bowl-of-shrimp-soup.html" >}}

## product

Configura la entrada como un producto, este modo aprovecha la [meta descripcion]({{< ref "config.md#habilitar-descripcion-de-búsqueda" >}}) y los [enlaces de adjunto]({{< ref "attachments.md" >}}).

{{< pagelink title="Demostración Product" name="Maily" href="https://maily.zkreations.com/2023/01/black-onyx-smartphone.html" >}}

## Combinaciones

Las plantillas de entrada se pueden combinar. Presta atención a la siguiente tabla de **combinaciones**. Un guión `-` indica que no tiene efecto al combinarse, si se puede combinar veras un `Si` y en caso de que no veras un `No`:

{{< table >}}
| Template       | `full`     | `centered` | `hero`     | `fixed`     | `featured` | `product`
| -------------- | ---------- | ---------- | ---------- | ---------- | ---------- | ----------
| `full`         | -          | -          | Si         | Si         | Si         | **No**    
| `centered`     | -          | -          | Si         | Si         | Si         | **No**    
| `hero`         | Si         | Si         | -          | Si         | **No**     | Si        
| `fixed`        | Si         | Si         | Si         | -          | Si         | Si        
| `featured`     | Si         | Si         | **No**     | Si         | -          | Si        
| `product`      | **No**     | **No**     | Si         | Si         | Si         | -         
{{< /table >}}

El orden de los valores no importa, tampoco es necesario agregar ningún carácter de separación, pero de todas formas recomendamos utilizar un guion **"-"** para separar cada plantilla de entrada especificada:

{{< pagelink title="Demostración Hero + Fixed" name="Maily" href="https://maily.zkreations.com/2022/11/airplane-among-green-trees-of-forest.html" >}}

{{< pagelink title="Demostración Hero + Fixed + Centered" name="Maily" href="https://maily.zkreations.com/2023/01/photo-of-white-flowers.html" >}}

## Sobrescribir valores

Los valores ingresados en esta variable **se pueden sobrescribir en entradas individuales**. Consulta la [sección templates]({{< ref "templates.md" >}}) para saber más.