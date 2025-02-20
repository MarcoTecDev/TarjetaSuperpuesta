# Proyecto de Animación con HTML y CSS

Este es un pequeño proyecto personal donde he experimentado con efectos visuales en CSS y HTML. Mi objetivo principal era lograr un efecto atractivo al pasar el ratón sobre una imagen, haciendo que esta cambie de perspectiva y revele otra imagen con una animación suave. Quería explorar cómo se pueden crear efectos llamativos solo con CSS, sin necesidad de JavaScript.

## Tecnologías Utilizadas

- **HTML**: Para definir la estructura de la página.
- **CSS**: Para los estilos y animaciones sin usar JavaScript.

## ¿Por qué este efecto?

Muchas veces, los efectos visuales complejos requieren el uso de JavaScript. Sin embargo, con las herramientas adecuadas de CSS, se pueden lograr transiciones fluidas y dinámicas sin afectar el rendimiento de la página. Además, CSS permite optimizar el renderizado en navegadores modernos, evitando sobrecargar el proceso de carga con scripts innecesarios.

## ¿Cómo funciona?

1. Dentro de un `<article>`, incluyo dos imágenes:
   - La primera imagen actúa como fondo y tiene una sombra para dar profundidad.
   - La segunda imagen (Tux) está oculta por defecto y se superpone a la primera cuando ocurre la interacción.

2. Uso `position: absolute` para colocar la imagen de Tux sobre la primera, de manera que pueda mostrarse solo cuando sea necesario.

3. Mediante la propiedad `opacity: 0`, la imagen de Tux está oculta hasta que el usuario pase el ratón sobre el artículo.

4. Cuando el usuario pasa el ratón:
   - Se aplica una transformación con `perspective`, `rotateX`, `translateY` y `translateZ` para dar un efecto 3D a la imagen.
   - La imagen de Tux cambia su opacidad a `1` y se desplaza ligeramente hacia arriba.
   - Se agrega un degradado que oscurece progresivamente la parte inferior del artículo, logrando un efecto más inmersivo.

## Notas y Avisos

- Este efecto funciona mejor en navegadores modernos como Chrome, Firefox y Edge. Internet Explorer puede no renderizar correctamente algunas propiedades de CSS.
- La transición está optimizada para que sea fluida, pero en dispositivos móviles podría no apreciarse igual que en pantallas grandes.
- Si deseas cambiar la imagen de fondo o el personaje, simplemente edita las rutas en el HTML.

## Archivos

### `index.html`
Aquí establezco la estructura básica del documento:

```html
<article>
    <img src="./Imgs/debian_wallpaper.jpg" alt="Fondo Debian">
    <img src="./Imgs/tux.png" alt="Tux">
</article>
```

### `style.css`
En este archivo aplico los estilos y animaciones:

```css
article:hover {
    transform:
        perspective(250px)
        rotateX(10deg)
        translateY(-5%)
        translateZ(0);
}

article:hover img:last-child {
    opacity: 1;
    transform: translateY(10%);
}
```

## ¿Cómo usarlo?
1. Clona el repositorio en tu ordenador:
   ```bash
   git clone https://github.com/mi-usuario/mi-repositorio.git
   ```
2. Abre `index.html` en tu navegador favorito.

Espero que este pequeño proyecto te sirva para entender mejor las posibilidades de CSS en animaciones sin JavaScript. ¡Disfrútalo!

