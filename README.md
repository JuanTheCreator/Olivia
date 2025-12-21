# OLIVIA MERINO - Tienda de Zapatos Premium

Una tienda de zapatos online moderna y elegante, con funcionalidades completas de e-commerce y diseño responsive.

## 🚀 Características

- **Catálogo de Productos**: 20 productos variados de zapatos para mujer, hombre y niños
- **Sistema de Filtros**: Por categoría, tipo y precio
- **Búsqueda en tiempo real**: Encuentra productos fácilmente
- **Carrito de Compras**: Persistente con LocalStorage
- **Diseño Responsive**: Funciona perfectamente en móviles, tablets y desktop
- **Animaciones Suaves**: Experiencia de usuario moderna
- **Preparado para BD**: Estructura escalable para migrar a base de datos

## 📁 Estructura del Proyecto

```
Olivia/
│
├── index.html              # Página principal
├── css/
│   └── styles.css         # Todos los estilos
├── js/
│   └── app.js             # Lógica de la aplicación
└── data/
    └── products.json      # Base de datos simulada (JSON)
```

## 🛠️ Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Grid, Flexbox, Animaciones
- **JavaScript ES6+**: Async/await, LocalStorage, Módulos
- **Font Awesome**: Iconos

## 🚦 Cómo Usar

### Opción 1: Servidor Local Simple

Abre una terminal en la carpeta del proyecto y ejecuta:

```bash
# Si tienes Python 3
python -m http.server 8000

# O si tienes Node.js
npx serve
```

Luego abre tu navegador en `http://localhost:8000`

### Opción 2: Abrir directamente

Simplemente abre `index.html` en tu navegador favorito.

## 📱 Funcionalidades Principales

### 1. Navegación y Búsqueda
- Barra de búsqueda en tiempo real
- Filtros por categoría (Mujer, Hombre, Niños)
- Filtros por tipo (Deportivo, Casual, Formal, Botas)
- Filtros por rango de precio

### 2. Carrito de Compras
- Añadir/eliminar productos
- Ajustar cantidades
- Total calculado automáticamente
- Guardado en LocalStorage (persiste al cerrar el navegador)

### 3. Diseño Responsive
- Mobile First
- Breakpoints: 480px, 768px, 1024px
- Menú hamburguesa en móviles
- Grid adaptable

## 🎨 Personalización

### Colores
Edita las variables CSS en `styles.css`:

```css
:root {
    --primary-color: #2c3e50;
    --secondary-color: #e74c3c;
    --accent-color: #3498db;
}
```

### Productos
Edita `data/products.json` para añadir, modificar o eliminar productos.

## 🔄 Migración a Base de Datos

Este proyecto está preparado para migrar fácilmente a una base de datos real:

### Opción 1: Node.js + Express + MongoDB

```javascript
// Ejemplo de endpoint
app.get('/api/products', async (req, res) => {
    const products = await Product.find();
    res.json({ products });
});
```

### Opción 2: Node.js + Express + PostgreSQL

```javascript
// Ejemplo de endpoint
app.get('/api/products', async (req, res) => {
    const result = await pool.query('SELECT * FROM products');
    res.json({ products: result.rows });
});
```

Solo necesitas cambiar en `app.js`:

```javascript
// De:
const response = await fetch('data/products.json');

// A:
const response = await fetch('/api/products');
```

## 📋 Próximas Mejoras Sugeridas

- [ ] Sistema de autenticación de usuarios
- [ ] Página de detalle de producto individual
- [ ] Sistema de reviews y valoraciones
- [ ] Integración con pasarela de pago (Stripe/PayPal)
- [ ] Panel de administración
- [ ] Wishlist (lista de deseos)
- [ ] Comparador de productos
- [ ] Sistema de cupones y descuentos
- [ ] Newsletter funcional
- [ ] Seguimiento de pedidos

## 🌐 Backend Sugerido (Opcional)

Para hacerlo completamente funcional con base de datos:

```bash
# Instalar dependencias
npm init -y
npm install express mongoose dotenv cors

# Crear servidor básico
node server.js
```

## 📝 Licencia

Este proyecto está creado para uso educativo y personal.

## 👤 Autor

**Olivia Merino Store**
- Tienda de zapatos premium
- Año: 2025

---

¡Disfruta de tu nueva tienda online! 🎉👟
