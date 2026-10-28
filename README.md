# Sumaventuras

Juego educativo en español para practicar las tablas de sumar del 1 al 9.

## Publicarlo con GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `sumaventuras`.
2. Sube `index.html` a la raíz del repositorio.
3. Entra en **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/(root)` y pulsa **Save**.
6. Espera unos minutos. GitHub mostrará la dirección pública en la sección Pages, normalmente:
   `https://TU-USUARIO.github.io/sumaventuras/`

No hace falta instalar dependencias ni ejecutar un servidor: es una web estática.

## Progreso

El juego guarda monedas, aciertos y medallas en `localStorage` del navegador. Ese progreso se guarda en ese navegador/dispositivo, no se sincroniza entre dispositivos.

## Personalización

Puedes editar los colores, nombres de los mundos y mensajes directamente en `index.html`.
