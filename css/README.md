# Estructura CSS Modular

## Archivos CSS Divididos

El archivo `styles.css` original (1695 líneas) ha sido dividido en 13 archivos modulares para mejor organización y mantenimiento:

### 📁 Estructura de Archivos

```
css/
├── base.css                 - Estilos base y reset (HTML, body, *)
├── header.css               - Header y navegación (nav, dropdown)
├── layout.css               - Layout de páginas (page, container, main-content, welcome)
├── sidebar.css              - Sidebar y estilos relacionados
├── footer.css               - Footer y copyright
├── images.css               - Imágenes y media components
├── buttons.css              - Back to top button y animaciones
├── responsive.css           - Media queries globales
├── australia.css            - Página Australia (sidebar derecho)
├── contact-blue.css         - Contact Us 1 (formulario azul)
├── contact-minimal.css      - Contact Us 2 (formulario minimalista)
├── booking.css              - Contact Us 3 (formulario de reserva)
└── job-application.css      - Contact Us 4 (formulario de aplicación)
```

### 🔄 Cómo Usar

**Opción 1: Usar el nuevo archivo principal (Recomendado)**
```html
<link rel="stylesheet" href="styles-new.css">
```

**Opción 2: Importar archivos individuales** 
```html
<link rel="stylesheet" href="css/base.css">
<link rel="stylesheet" href="css/header.css">
<link rel="stylesheet" href="css/layout.css">
<!-- ... resto de archivos según necesites -->
```

### ✅ Ventajas de la Estructura Modular

1. **Mantenimiento más fácil** - Encuentra estilos específicos rápidamente
2. **Desarrollo en equipo** - Múltiples personas pueden trabajar en diferentes archivos
3. **Carga selectiva** - Importa solo los estilos que necesitas en cada página
4. **Depuración simplificada** - Errores más fáciles de localizar
5. **Mejor organización** - Cada archivo tiene un propósito claro

### 📋 Orden de Importación

El orden de los @import en `styles-new.css` es importante:

1. **Base** - Reset y estilos fundamentales primero
2. **Layout** - Estructura general de la página
3. **Components** - Componentes reutilizables
4. **Pages** - Estilos específicos de páginas
5. **Responsive** - Media queries al final para sobrescribir cuando sea necesario

### 🔧 Migración

Para migrar de `styles.css` antiguo a la nueva estructura:

1. Reemplaza `<link rel="stylesheet" href="styles.css">` por `<link rel="stylesheet" href="styles-new.css">`
2. Verifica que todos los estilos se apliquen correctamente
3. Una vez confirmado, puedes renombrar `styles.css` a `styles-old.css` como backup
4. Renombra `styles-new.css` a `styles.css`

### 📝 Notas

- Todos los archivos mantienen los mismos estilos exactos del archivo original
- No se ha modificado ninguna funcionalidad, solo la organización
- Los comentarios de sección se mantienen en cada archivo
- El archivo `styles.css` original se conserva como backup
