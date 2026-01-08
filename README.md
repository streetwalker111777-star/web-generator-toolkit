# 📸 Mi Galería Personal Multimedia

> Una galería web moderna y responsiva para mostrar fotos y videos personales

## 🌟 Descripción

Este proyecto es una galería multimedia personal construida con HTML, CSS y JavaScript puro. Perfecta para compartir recuerdos, momentos especiales y contenido multimedia de forma elegante y profesional.

## ✨ Características

- 📱 **Diseño Responsivo**: Se adapta perfectamente a móviles, tablets y escritorio
- 🎨 **Interfaz Moderna**: Diseño limpio con tipografía Inter de Google Fonts
- 🖼️ **Galería de Fotos**: Visualización optimizada de imágenes con lazy loading
- 🎬 **Reproductor de Videos**: Soporte nativo para videos MP4 con controles
- ⚡ **Rendimiento Optimizado**: Carga rápida y eficiente
- 🌐 **Desplegado en GitHub Pages**: Accesible desde cualquier lugar

## 📁 Estructura del Proyecto

```
web-generator-toolkit/
├── css/
│   └── style.css          # Estilos personalizados
├── js/
│   └── main.js            # Scripts JavaScript
├── images/
│   └── *.jpg              # Imágenes de la galería
├── videos/
│   └── *.mp4              # Videos multimedia
├── .github/
│   └── workflows/
│       └── pages.yml      # Workflow de despliegue automático
├── .nojekyll              # Archivo para GitHub Pages
├── index.html             # Página principal
└── README.md              # Este archivo
```

## 🚀 Despliegue

Este sitio está configurado para desplegarse automáticamente en GitHub Pages:

### URL del sitio publicado:
**https://streetwalker111777-star.github.io/web-generator-toolkit/**

### Proceso de Despliegue Automático

1. Cualquier cambio en la rama `main` activa el workflow de GitHub Actions
2. El sitio se construye y despliega automáticamente
3. Disponible en minutos tras cada commit

## 💻 Uso Local

Para ejecutar este proyecto localmente:

```bash
# Clonar el repositorio
git clone https://github.com/streetwalker111777-star/web-generator-toolkit.git

# Navegar al directorio
cd web-generator-toolkit

# Abrir con un servidor local (ejemplo con Python)
python -m http.server 8000

# O simplemente abrir index.html en tu navegador
```

## 🛠️ Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos con Grid y Flexbox
- **JavaScript**: Interactividad y funcionalidad
- **Google Fonts**: Tipografía Inter
- **GitHub Pages**: Hosting gratuito
- **GitHub Actions**: CI/CD automatizado

## 📝 Personalización

### Añadir Nuevas Imágenes

1. Coloca tus imágenes en la carpeta `images/`
2. Edita `index.html` y añade:

```html
<div class="photo-card">
  <img src="images/tu-imagen.jpg" alt="Descripción" loading="lazy">
</div>
```

### Añadir Nuevos Videos

1. Coloca tus videos en la carpeta `videos/`
2. Edita `index.html` y añade:

```html
<div class="video-card">
  <video controls>
    <source src="videos/tu-video.mp4" type="video/mp4">
    Tu navegador no soporta el elemento de video.
  </video>
  <div class="caption">Título del Video</div>
</div>
```

## 🔧 Configuración de GitHub Pages

El sitio está configurado con:
- **Source**: Deploy from a branch
- **Branch**: `main`
- **Folder**: `/` (root)

## 📄 Licencia

Este proyecto es de código abierto y está disponible para uso personal.

## 👤 Autor

**Miguel Angel** (streetwalker111777-star)
- GitHub: [@streetwalker111777-star](https://github.com/streetwalker111777-star)

## 🎯 Próximas Mejoras

- [ ] Modal para vista ampliada de imágenes
- [ ] Filtros y categorías para organizar contenido
- [ ] Galería de videos mejorada con miniaturas
- [ ] Modo oscuro/claro
- [ ] Animaciones y transiciones suaves
- [ ] Optimización de imágenes automática
- [ ] Sistema de comentarios

---

⭐ Si te gusta este proyecto, ¡dale una estrella en GitHub!
