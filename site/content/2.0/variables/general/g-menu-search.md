---
title: g.menuSearch
weight: 3
---

Habilita el botón que muestra el buscador en el header, visible en todos los tipos de página.

```html
<Variable name="g.menuSearch" description="Enable search in menu" type="string" value="true"/>
```

## Valores disponibles

Si el valor ingresado no es válido, el valor por defecto será `true`.

{{< table >}}
| Value          | Nombre    | Tipo                    | Descripción   
| -------------- | ----------| ------------------------| --------------
| `true` `yes`   | Verdadero | {{< data boolean >}}    | Habilita el botón de búsqueda en el menú
| `false` `no`   | Falso     | {{< data boolean >}}    | Deshabilita el botón de búsqueda en el menú
{{< /table >}}


## true

El botón que muestra el formulario de búsqueda en la barra de menú será visible en la sección secundaria del menú principal y estará disponible en cualquier página del blog.


![g-modal-search](/images/variables/general/g-modal-search.png)


## false

El botón y el formulario de búsqueda en el menú no estará disponible en el blog.
