# 🛍️ Panel de Administración - Vívelo Store

## Descripción

El Panel de Administración es una herramienta completa para gestionar todos los aspectos de la tienda online Vívelo Store. Permite administrar productos, carrusel, configuración general y más, todo desde una interfaz moderna e intuitiva.

## 🚀 Acceso Rápido

### Credenciales por Defecto
- **Usuario:** `admin`
- **Contraseña:** `vivelo2025`

### Archivos del Sistema
- `admin.html` - Panel de administración
- `tienda.html` - Tienda online (frontend)
- `products.json` - Datos de productos (carga inicial)
- `slider.json` - Datos del carrusel (carga inicial)
- `config.json` - Configuración general (carga inicial)

## 📁 Estructura de Datos

### Productos (`products.json`)
```json
{
  "products": [
    {
      "id": 1,
      "name": "Nombre del Producto",
      "category": "Categoría",
      "price": 99.99,
      "description": "Descripción del producto",
      "videoUrl": "https://url-del-video.mp4",
      "posterUrl": "https://url-de-imagen.jpg"
    }
  ]
}
```

### Carrusel (`slider.json`)
```json
{
  "slides": [
    {
      "id": 1,
      "title": "Título del Slide",
      "description": "Descripción del slide",
      "imageUrl": "https://url-de-imagen.jpg"
    }
  ]
}
```

### Configuración (`config.json`)
```json
{
  "store": {
    "name": "Nombre de la Tienda",
    "phone": "+1 234 567 8900",
    "email": "contacto@tienda.com",
    "address": "Dirección física",
    "mapsUrl": "https://maps.google.com/...",
    "logoUrl": "https://url-del-logo.png"
  },
  "theme": {
    "primaryColor": "#2563eb",
    "darkColor": "#1e40af",
    "lightColor": "#f8fafc"
  },
  "categories": ["Categoría 1", "Categoría 2"]
}
```

## 🎯 Funcionalidades

### 1. Sistema de Autenticación
- Login seguro con validación de credenciales
- Sesión persistente usando localStorage
- Timeout automático después de 30 minutos de inactividad
- Opción para cambiar contraseña

### 2. Dashboard
- Vista general de estadísticas:
  - Total de productos
  - Categorías disponibles
  - Slides del carrusel
  - Última modificación
- Acciones rápidas para crear productos y editar configuración
- Botones de importar/exportar datos

### 3. Gestión de Productos
- **Listado completo** con:
  - Miniatura del producto
  - Nombre y categoría
  - Precio
  - Acciones de editar/eliminar
- **Filtros y búsqueda:**
  - Búsqueda por nombre
  - Filtro por categoría
- **Formulario de producto:**
  - Nombre del producto
  - Categoría (seleccionable)
  - Precio
  - Descripción
  - URL de video
  - URL de imagen de portada
  - Vista previa en tiempo real

### 4. Gestión de Carrusel
- Vista de cards para cada slide
- Edición de:
  - Título
  - Descripción
  - Imagen de fondo
- Vista previa de imagen

### 5. Configuración General
- **Información de la tienda:**
  - Nombre
  - Teléfono
  - Email
  - Dirección
  - URL de Google Maps
  - Logo
- **Colores del tema:**
  - Color primario
  - Color oscuro
  - Color claro
  - Vista previa de colores
- **Categorías:**
  - Gestión de categorías disponibles

### 6. Seguridad
- Cambio de contraseña
- Información de sesión actual
- Protección contra timeout

## 💾 Importar/Exportar Datos

### Exportar
1. Ve al Dashboard
2. Haz clic en "📥 Exportar Datos"
3. Se descargará un archivo JSON con todos los datos

### Importar
1. Ve al Dashboard
2. Haz clic en "📤 Importar Datos"
3. Selecciona un archivo JSON válido
4. Los datos se cargarán automáticamente

## 🛒 Tienda Online (tienda.html)

La tienda online lee automáticamente los datos desde localStorage, lo que significa que cualquier cambio hecho en el panel de administración se refleja inmediatamente.

### Características de la Tienda:
- Header con navegación y carrito
- Carrusel de imágenes promocionales
- Grid de productos con filtro por categoría
- Reproducción de video al hover
- Carrito de compras lateral
- Checkout via WhatsApp
- Footer con información de contacto
- Diseño totalmente responsive

## 🎨 Personalización del Tema

Los colores del tema se pueden modificar desde:
1. Panel de Admin → Configuración General → Colores del Tema
2. Selecciona los colores deseados
3. Guarda los cambios
4. Abre la tienda para ver los cambios aplicados

## 📱 Compatibilidad

El panel y la tienda son compatibles con:
- ✅ Google Chrome (última versión)
- ✅ Mozilla Firefox (última versión)
- ✅ Safari (última versión)
- ✅ Microsoft Edge (última versión)
- ✅ Dispositivos móviles y tablets

## 🔧 Almacenamiento

Todos los datos se almacenan en el localStorage del navegador:

| Clave | Descripción |
|-------|-------------|
| `vivelotv_products` | Lista de productos |
| `vivelotv_slides` | Slides del carrusel |
| `vivelotv_config` | Configuración general |
| `vivelotv_credentials` | Credenciales de admin |
| `vivelotv_session` | Sesión actual |
| `vivelotv_lastModified` | Fecha de última modificación |
| `vivelotv_cart` | Carrito de compras (tienda) |

## ⚠️ Notas Importantes

1. **Backup:** Se recomienda exportar los datos periódicamente como respaldo.
2. **Navegador:** Los datos se almacenan en el navegador, si cambias de navegador o limpias los datos, se perderá la información.
3. **Primera carga:** En la primera ejecución, se cargan los datos desde los archivos JSON como valores por defecto.
4. **Seguridad:** Las credenciales se almacenan localmente. En un entorno de producción real, se recomienda implementar autenticación del lado del servidor.

## 🆘 Solución de Problemas

### Los datos no aparecen
1. Verifica que los archivos JSON estén en la misma carpeta
2. Limpia el localStorage y recarga la página
3. Revisa la consola del navegador para errores

### No puedo iniciar sesión
- Usuario por defecto: `admin`
- Contraseña por defecto: `vivelo2025`
- Si cambiaste la contraseña y la olvidaste, limpia el localStorage

### Los cambios no se reflejan en la tienda
1. Asegúrate de guardar los cambios en el panel
2. Recarga la página de la tienda
3. Verifica que estés usando el mismo navegador

## 📞 Soporte

Para soporte técnico o preguntas, contacta a través de los canales de la tienda configurados en el panel de administración.

---

**Versión:** 1.0.0  
**Última actualización:** Noviembre 2024
