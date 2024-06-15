# Convencion de estilos

 Ahora, vas a crear los estilos base y variables que usaremos en todo nuestro proyecto.

Cómo hacer el posicionamiento de contenido
Como parte de las buenas prácticas tenemos un orden en que es recomendable escribir el código dentro de CSS. Te ayudarán a tener todas las secciones organizadas y saber dónde regresar cuando necesites hacer un cambio o solucionar un problema.

- Posicionamiento --> static, absolute, relative, fixed.
- Modelo de caja (Box model) --> margin, border, padding, content.
- Tipografía --> tipos, tamaños de fuente, etc.
- Estilos visuales --> box-shadow, border-radius, gradient, etc.
- Otros --> misceláneos, reglas CSS y más.


# background en hero

## Uso de `linear-gradient`

El linear-gradient es una función en CSS que crea una imagen de gradiente que varía en color a lo largo de una línea recta. Puedes usarla como valor para propiedades que aceptan imágenes, como background-image, border-image, o mask-image.

Aquí tienes la sintaxis básica y algunos ejemplos para entender cómo funciona:

- **Sintaxis basica**

```
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
```

- direction: Define la dirección del gradiente. Puede ser un ángulo (e.g., 45deg), palabras clave (to right, to bottom, etc.), o por defecto, se usa to bottom.
- color-stop: Define los colores en el gradiente, y opcionalmente, el punto en el que se alcanzan esos colores (e.g., red 10%, blue 90%).

- **Gradiente de izquierda a derecha**

Este gradiente comienza con red en el lado izquierdo y cambia gradualmente a blue en el lado derecho.
`background-image: linear-gradient(to right, red, blue);`

## linear gradient en Hero

- **Gradiente en un ángulo específico**

`background-image: linear-gradient(45deg, red, blue);`

Este gradiente sigue una línea de 45 grados desde la esquina superior izquierda a la esquina inferior derecha, cambiando de red a blue.

- Codigo de proyecto

```
 position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2.5rem;
    padding-bottom: 6rem;
    text-align: center;
    background-image: linear-gradient(207.8deg, var(--warm-black) 16.69%,var(--bitcoin-orange) 100% );
```

1. ` linear-gradient(207.8deg, ... )`: La función linear-gradient se utiliza para crear una imagen de gradiente que cambia de color a lo largo de una línea recta. El primer parámetro de esta función es la dirección del gradiente.

- `207.8deg`: Este valor indica el ángulo del gradiente. En lugar de utilizar direcciones predefinidas (como to right, to bottom, etc.), se usa un ángulo específico. El ángulo se mide en grados, comenzando desde la parte superior (0 grados) y girando en el sentido de las agujas del reloj. Así, 207.8deg crea una línea de gradiente que está inclinada 207.8 grados desde la parte superior.

2. `var(--warm-black) 16.69%`: Este es el primer "color-stop" del gradiente.

- `var(--warm-black)`: Utiliza una variable CSS. Las variables CSS (o custom properties) se definen en el :root o en un selector específico usando la sintaxis --variable-name. En este caso, --warm-black es el nombre de la variable que contiene un valor de color.

- `16.69%`: Este valor indica que el color --warm-black debería estar completamente presente hasta el 16.69% del camino a lo largo de la línea del gradiente.

3. `var(--bitcoin-orange) 100%`: Este es el segundo "color-stop" del gradiente.

- `var(--bitcoin-orange)`: Utiliza otra variable CSS para el color. En este caso, --bitcoin-orange es el nombre de la variable que contiene otro valor de color.

- `100%`: Este valor indica que el color --bitcoin-orange debería estar presente desde el 16.69% hasta el 100% del camino a lo largo de la línea del gradiente, completando el gradiente.

