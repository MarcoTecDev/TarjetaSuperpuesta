# Proyecto de Animación con HTML y CSS

Este proyecto muestra cómo crear un efecto visual atractivo usando HTML y CSS. Cuando pasas el cursor sobre una imagen, esta cambia de perspectiva y muestra otra imagen con un efecto de transición.

## Tecnologías Usadas

- **HTML**: Estructura del documento.
- **CSS**: Estilos y animaciones.

## Funcionamiento

1. Se muestran dos imágenes dentro de un `<article>`.
2. La primera imagen (de fondo) tiene sombras y bordes redondeados.
3. La segunda imagen (Tux) está oculta inicialmente con `opacity: 0` y se posiciona con `absolute`.
4. Al pasar el mouse por el artículo:
   - Se aplica una transformación en perspectiva y rotación.
   - Se muestra la imagen de Tux con una transición suave.
   - Se oscurece el fondo gradualmente con un degradado.

## Archivos

### `index.html`
Estructura básica con un `<article>` que contiene dos imágenes.

```html
<article>
    <img src="./Imgs/debian_wallpaper.jpg" alt="Fondo Debian">
    <img src="./Imgs/tux.png" alt="Tux">
</article>
```

### `style.css`
Define la apariencia y las animaciones:

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

## Cómo Usarlo
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/tu-repositorio.git
   ```
2. Abre `index.html` en tu navegador.

¡Disfruta del efecto visual!

