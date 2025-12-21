# 🎨 Sistema Modular - Olivia Merino

## 📁 Nueva Estructura de Archivos

```
Olivia/
├── assets/
│   └── images/
│       ├── hero/               # Imágenes del hero slider
│       │   ├── slide1.png
│       │   └── slide2.png
│       ├── editorial/          # Imágenes de secciones editoriales
│       │   ├── hombre.jpeg
│       │   ├── mujer.jpeg
│       │   ├── slide-mujer.png
│       │   └── slide-hombre.png
│       ├── services/           # Imágenes de historia/servicios
│       │   ├── ideas.jpeg
│       │   ├── historia.png
│       │   └── marca.png
│       └── products/           # Imágenes de productos (futuro)
│
├── css/
│   ├── main.css               # ✨ Archivo principal con imports
│   ├── styles.css             # ⚠️ Archivo antiguo (mantener por ahora)
│   └── modules/               # 📦 Módulos CSS
│       ├── variables.css      # Variables globales
│       ├── reset.css          # Reset y estilos base
│       ├── header.css         # Header y navegación
│       ├── hero.css           # Hero section
│       ├── editorial.css      # Secciones editoriales
│       ├── services.css       # Servicios/Historia
│       ├── products.css       # Productos
│       ├── footer.css         # Footer
│       ├── modals.css         # Modales
│       └── responsive.css     # Media queries
│
├── js/
│   └── app.js
│
├── data/
│   └── products.json
│
├── index.html
├── productos.html
└── README.md
```

## 🎯 Ventajas del Sistema Modular

### 1. **Escalabilidad**
- Cada módulo es independiente
- Fácil agregar nuevas secciones sin tocar código existente
- Archivos más pequeños y manejables

### 2. **Mantenibilidad**
- Cambios aislados por módulo
- Fácil encontrar y modificar estilos específicos
- Menos conflictos en equipo

### 3. **Performance**
- Posibilidad de cargar módulos bajo demanda
- Optimización por sección
- Minificación modular

### 4. **Organización**
- Estructura clara y lógica
- Nombres descriptivos
- Separación de responsabilidades

## 📝 Cómo Usar

### Para desarrollo (usar main.css):
```html
<link rel="stylesheet" href="css/main.css">
```

### Para producción (usar styles.css actual):
```html
<link rel="stylesheet" href="css/styles.css">
```

## 🔄 Migración Gradual

1. **Fase 1** (Actual): Crear estructura modular
2. **Fase 2**: Migrar secciones una por una
3. **Fase 3**: Probar y validar cada módulo
4. **Fase 4**: Eliminar styles.css antiguo

## 🖼️ Organización de Imágenes

### Convención de nombres:
- **hero/**: `slide{número}.png`
- **editorial/**: `{categoría}.{formato}`
- **services/**: `{concepto}.{formato}`
- **products/**: `{sku}-{vista}.{formato}`

### Rutas actualizadas:
```html
<!-- Antes -->
<img src="public/image.png">

<!-- Ahora -->
<img src="assets/images/hero/slide1.png">
```

## 🚀 Próximos Pasos

1. Crear módulos CSS restantes
2. Actualizar referencias de imágenes en HTML
3. Documentar cada módulo
4. Agregar comentarios detallados
5. Optimizar assets

## 📦 Build Process (Futuro)

Para cuando el proyecto crezca:
- Usar preprocesadores (SCSS/SASS)
- Build tools (Webpack/Vite)
- Minificación automática
- Compresión de imágenes
- Cache busting
