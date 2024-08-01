# README

## Inicialización del Proyecto

Para comenzar, inicializa tu proyecto npm si aún no lo has hecho, la carpeta vacia de tu proyecto ejecuta:

```bash
npm init -y
```

## Instalación de Dependencias

1. **Instalar Bootstrap:**

    ```bash
    npm install bootstrap
    ```

2. **Instalar Sass (si aún no está instalado):**

    ```bash
    npm install sass
    ```

## Configuración de Sass

1. **Importar Bootstrap en Sass:**

    En tu archivo principal de Sass (por ejemplo, `./assets/scss/main.scss`), agrega:

    ```scss
        @import "../../node_modules/bootstrap/scss/bootstrap.scss"
    ```

2. **Agregar un Script en `package.json` para Compilar Sass a CSS:**

    En tu archivo `package.json`, agrega el siguiente script dentro de la sección `"scripts"`:

    ```json
    "scripts": {
      "build-css": "sass assets/scss:assets/css"
    }
    ```

3. **Ejecutar el Script para Compilar Sass a CSS:**

    Ejecuta el siguiente comando para compilar tus archivos Sass a CSS:

    ```bash
    npm run build-css
    ```
## Alternativa de compilación de Sass
1. **Recuerda que puedes usar el plug-in de Live Sass Compiler:**
    [Link de MarketPlace Studio](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)
   

 
## Estructura del Proyecto

La estructura recomendada para tu proyecto es la siguiente:

```bash
/project
├── /assets
│   ├── /css         # Archivos CSS compilados
│   ├── /js          # Archivos JavaScript
│   └── /scss        # Archivos Sass
│       ├── /abstracts
│       │   ├── _variables.scss   # Define variables globales
│       │   ├── _mixins.scss      # Define mixins reutilizables
│       │   └── _functions.scss   # Define funciones Sass personalizadas
│       ├── /base
│       │   ├── _reset.scss        # Resetea estilos predeterminados del navegador
│       │   ├── _typography.scss   # Estilos básicos de tipografía
│       │   └── _base.scss         # Estilos base para elementos HTML
│       ├── /components
│       │   ├── _buttons.scss      # Estilos para botones
│       │   ├── _cards.scss        # Estilos para tarjetas
│       │   └── _forms.scss        # Estilos para formularios
│       ├── /layout
│       │   ├── _header.scss       # Estilos para el encabezado
│       │   ├── _footer.scss       # Estilos para el pie de página
│       │   ├── _sidebar.scss      # Estilos para la barra lateral
│       │   └── _grid.scss         # Estilos para el sistema de rejilla
│       ├── /pages
│       │   ├── _home.scss         # Estilos específicos para la página de inicio
│       │   ├── _about.scss        # Estilos específicos para la página de "Sobre nosotros"
│       │   └── _contact.scss      # Estilos específicos para la página de contacto
│       └── /themes
│           ├── _default.scss      # Estilos para el tema predeterminado
│           └── _dark.scss         # Estilos para el tema oscuro
│       ├── /main.scss             # Manifiesto donde se deben importar todos los parciales 

├── index.html          # Archivo HTML principal
├── package.json        # Archivo de configuración de npm
└── /node_modules       # Dependencias de npm
```

## Configuración de JavaScript
1. **Importar Bundle de Bootstrap en script.js:**

    En tu archivo principal de js (por ejemplo, `./assets/js/script.js`), agrega:

    ```js
        import "../../node_modules/bootstrap/dist/js/bootstrap.bundle.js";
    ```
2. **Importar Script.js en Index:**

    En tu archivo principal de HTML (por ejemplo, `./index.html`), agrega:

    ```html
        <script type="module" src="./assets/js/script.js"></script>
    ```

    *Recuerda que el script debe contener la propiedad `type="module"`

## Habilitar un componente de Bootstrap que usa JavaScript
1. **En el caso de usar Tooltip que es un elemento que requiere habilitarse:**

    En tu archivo principal de js (por ejemplo, `./assets/js/script.js`), agrega:

    ```js
        const popoverTriggerList = document.querySelectorAll('[data-bs-toggle="popover"]')
        const popoverList = [...popoverTriggerList].map(popoverTriggerEl => new bootstrap.Popover(popoverTriggerEl))
    ```
    El código para habilitar el componente siempre lo encontraras en las sección ` Enable {Nombre del Componente}`

    Te dejo el link de la documentación de Tooltips para que lo puedas comprobar [Tooltip-Boostrap](https://getbootstrap.com/docs/5.3/components/popovers/)
 

¡Listo! Ahora estás listo para desarrollar tu proyecto con Bootstrap y Sass.
