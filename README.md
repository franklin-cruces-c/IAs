# 🤖 Directorio de IAs

Una aplicación web estática que sirve como directorio organizado de herramientas de Inteligencia Artificial, clasificadas por su modelo de acceso (gratis, trial, pago) y funcionalidad.

## ✨ Características

- **Clasificación inteligente**: Herramientas organizadas por categoría y modelo de precios
- **Filtros dinámicos**: Buscar por nombre, filtrar por categoría y modelo de acceso
- **Vista detallada**: Información completa de cada herramienta en modal
- **Modo inmersivo**: Visualizar herramientas directamente en iframe (cuando lo permite el sitio)
- **Interfaz moderna**: Diseño oscuro con transiciones suaves y animaciones
- **Totalmente estático**: Solo HTML, CSS y JavaScript puro - no requiere servidor ni build

## 🚀 Uso

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/directorio-ias.git
   ```

2. Abrir `DirectorioIAs.html` o `DirectorioIAs` en cualquier navegador web moderno

3. ¡Explorar! Usa la barra de búsqueda y los filtros para encontrar herramientas

## 📂 Estructura del proyecto

```
.
├── DirectorioIAs.html      # Archivo HTML principal (copia de trabajo)
├── DirectorioIAs           # Versión minificada o alternativa
├── README.md               # Este archivo
└── .git/                   # Repositorio Git
```

## 🔧 Cómo agregar nuevas herramientas

El directorio está diseñado para ser fácilmente extensible. Para agregar una nueva IA:

1. Abrir el archivo HTML en un editor de texto
2. Buscar el array `aiTools` alrededor de la línea 450
3. Añadir un nuevo objeto siguiendo este formato:
   ```javascript
   {
     id: "identificador-unico", 
     name: "Nombre de la Herramienta",
     category: "categoria", // general, imagenes-video, audio-musica, programacion, etc.
     priceModel: "free", // free, trial o paid
     short: "Descripción breve de una línea.",
     full: "Descripción completa que aparecerá en el modal.",
     limits: "Información sobre límites o condiciones de uso.",
     url: "https://sitio-web-oficial.com"
   }
   ```
4. Las categorías disponibles están definidas en el objeto `categories`
5. Guardar el archivo y recargar en el navegador

## 📊 Modelo de datos

Cada herramienta en el array `aiTools` tiene los siguientes campos:
- `id`: Identificador único (string)
- `name`: Nombre visible de la herramienta (string)
- `category`: Categoría funcional (debe coincidir con las keys en `categories`)
- `priceModel`: Modelo de acceso (`free`, `trial` o `paid`)
- `short`: Descripción breve para la tarjeta (string)
- `full`: Descripción detallada para el modal (string)
- `limits`: Información sobre límites de uso (string)
- `url`: URL oficial de la herramienta (string)

## 🛠️ Tecnologías utilizadas

- HTML5 semántico
- CSS3 con variables personalizadas
- JavaScript vanilla (ES6+)
- Diseño responsive
- Animaciones CSS
- LocalStorage (para estado de filtros, si se implementa en el futuro)

## 📱 Compatibilidad

Funciona en todos los navegadores modernos:
- Chrome ✅
- Firefox ✅
- Safari ✅
- Edge ✅

## 📝 Notas importantes

- Los planes y límites de las herramientas de IA cambian frecuentemente. Siempre verifique la información en los sitios oficiales.
- Algunas herramientas pueden requerir registro o tener limitaciones regionales.
- El modo inmersivo (iframe) depende de las políticas de seguridad del sitio de destino (X-Frame-Options, CSP, etc.)

## 👥 Contribuir

Si deseas contribuir:
1. Haz fork del repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-herramienta`)
3. Agrega las herramientas siguiendo el formato especificado
4. Haz commit de tus cambios
5. Push a tu rama
6. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo licencia MIT - siéntete libre de usarlo, modificarlo y distribuirlo.

---

*Actualizado: Septiembre 2026*