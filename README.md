# Píldora Factoría F5 - Grid
Simone Ávila Arranz

## Descripción

Grid es algo conocido como grid based layout system, una técnica de diseño que organiza los elementos visuales en una estructura de filas y columnas, buscando coherencia, alineación, equilibrio y jerarquía visual. Funciona a través de la característica display: grid de CSS.

## Cómo utilizar Grid

### HTML

1. Crear un contenedor padre con la etiqueta div, añadir una clase.
```
<div class="padre"> </div>
```

2. Crear los hijos dentro con otros div, añadir clases individuales.
```
<div class="uno">1</div>"
```

3. Añadir el contenido deseado, en este caso los números del 1 al 5 y un Lorem Ipsum corto.

<img src="./imgs/1.jpg" alt="">

### CSS

1. Añadir la característica grid-area a las clases de los hijos.
```.uno {grid-area: uno;}
```

3. Añadir las características display: grid, grid-gap y grid-template-areas para establecer el grid, definir el espacio entre hijos y su orden, respectivamente. También personalizar como sea deseado. Ahora mismo el grid tiene una sola columna, más adelante utilizaremos media querys para adaptar el diseño a diferentes tamaños de pantalla.
```.padre {.padre
    color: white;
    display: grid;
    grid-gap: 1em;
    grid-template-areas:
        "uno"
        "dos"
        "tres"
        "cuatro"
        "cinco"
    }
```

3. Personalizar las celdas.
```.box {
    background-color: black;
    border-radius: 5px;
    padding: 10px;
    font-size: 150%; 
    }

.uno {
    background-color: red;
    }

.dos, .cuatro {
    background-color: green;
    }

.cinco {
    background-color: blue;
    }
```

<img src="./imgs/2.jpg" alt="">

4. Añadir media-query para que el diseño sea responsive en tablets y dispositivos móviles. Utilizar grid-template-columns y de nuevo grid-template-areas para establecer el número de columnas y el orden de los hijos, respectivamente.
```@media only screen and (min-width: 600px)  {
    .padre {
        grid-template-columns: 20% auto;
        grid-template-areas:
        "uno uno"
        "dos tres"
        "cuatro cuatro"
        "cinco cinco";
    }
}
```

<img src="./imgs/3.jpg" alt="">

```@media only screen and (min-width: 800px)   {
    .padre {
        grid-gap: 20px;
        grid-template-columns: 120px auto 120px;
        grid-template-areas:
        "uno uno uno"
        "dos tres cuatro"
        "cinco cinco cinco";
        max-width: 600px;
    }
}
```

<img src="./imgs/4.jpg" alt="">

## Recursos

- https://gridbyexample.com/
- https://www.w3schools.com/css/css_grid.asp
- https://alistapart.com/article/the-story-of-css-grid-from-its-creators/
