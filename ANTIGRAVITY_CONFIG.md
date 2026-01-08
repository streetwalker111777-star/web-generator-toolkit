# Configuración de Antigravity para Colaboración con Comet

## 📋 Instrucciones para Antigravity

Este repositorio está configurado para la colaboración automática entre **Antigravity** (add-on de Chrome) y **Comet** (asistente AI de Perplexity).

## 🎯 Estructura del Repositorio

```
web-generator-toolkit/
├── css/              # Archivos CSS (estilos)
├── js/               # Archivos JavaScript (scripts)
├── images/           # Imágenes y recursos gráficos
├── .github/
│   └── workflows/    # GitHub Actions para automatización
└── README.md         # Documentación principal
```

## 🚀 Workflow Automático

### ¿Qué sucede cuando Antigravity sube archivos?

1. **Detección automática**: GitHub Actions detecta cambios en `css/`, `js/` o `images/`
2. **Validación**: Se validan los archivos subidos
3. **Análisis**: Se genera un reporte de estructura
4. **Notificación**: Comet recibe información para análisis

### Eventos que activan el workflow:

- ✅ Push a la rama `main` o `dev`
- ✅ Pull requests
- ✅ Ejecución manual desde GitHub Actions

## 📝 Guía de Uso para Antigravity

### Paso 1: Subir Archivos

Antigravity puede subir archivos a través de:

1. **Commits directos** a la rama `main`
2. **Pull requests** para revisión antes de merge
3. **API de GitHub** (recomendado para automatización)

### Paso 2: Estructura de Carpetas

**CSS**: Coloca archivos en `css/`
```
css/
├── style.css
├── responsive.css
└── animations.css
```

**JavaScript**: Coloca archivos en `js/`
```
js/
├── main.js
├── utils.js
└── components.js
```

**Imágenes**: Coloca archivos en `images/`
```
images/
├── logo.png
├── banner.jpg
└── icons/
    ├── home.svg
    └── menu.svg
```

### Paso 3: Commits Descriptivos

Usa mensajes de commit claros:

✅ Bueno: `"Add responsive navigation styles"`
✅ Bueno: `"Update hero image and optimize size"`
❌ Malo: `"update"`
❌ Malo: `"changes"`

## 🔧 Configuración de la API de GitHub

### Autenticación

Para que Antigravity suba archivos automáticamente:

1. Genera un **Personal Access Token** en GitHub:
   - Ve a: Settings → Developer settings → Personal access tokens
   - Selecciona: `repo` (acceso completo al repositorio)
   - Guarda el token de forma segura

2. Configura Antigravity con:
   ```json
   {
     "repository": "streetwalker111777-star/web-generator-toolkit",
     "branch": "main",
     "token": "TU_TOKEN_AQUI"
   }
   ```

### Ejemplo de API Call desde Antigravity

```javascript
// Subir archivo a GitHub
const uploadFile = async (path, content, message) => {
  const url = `https://api.github.com/repos/streetwalker111777-star/web-generator-toolkit/contents/${path}`;
  
  const response = await fetch(url, {
    method: 'PUT',
    headers: {
      'Authorization': `token YOUR_TOKEN`,
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      message: message,
      content: btoa(content), // Base64 encode
      branch: 'main'
    })
  });
  
  return response.json();
};

// Uso
await uploadFile(
  'css/style.css',
  '.container { width: 100%; }',
  'Add container styles'
);
```

## 🤝 Colaboración con Comet

### Cómo Comet Analiza los Cambios

1. **Acceso a GitHub**: Comet puede ver el repositorio y los archivos
2. **Lectura de Reportes**: Comet lee los reportes generados por GitHub Actions
3. **Análisis de Código**: Comet puede revisar CSS, JS e imágenes
4. **Feedback**: Comet proporciona sugerencias de mejora

### Flujo de Trabajo Completo

```
[TÚ trabaja en local] ←→ [Antigravity sube a GitHub]
                              ↓
                    [GitHub Actions se ejecuta]
                              ↓
                    [Se genera reporte de análisis]
                              ↓
                    [Comet revisa y analiza]
                              ↓
                    [Tú recibes feedback]
```

## 📊 Monitoreo

### Ver el estado del workflow

1. Ve a la pestaña **Actions** en GitHub
2. Verás todos los workflows ejecutados
3. Haz clic en cualquiera para ver detalles
4. Descarga los reportes de análisis (artifacts)

### Ejemplo de Reporte

Cada ejecución genera:

- **ANALYSIS_REPORT.md**: Lista de archivos y estructura
- **Logs detallados**: Validación de CSS, JS e imágenes
- **Timestamps**: Cuándo se ejecutó cada paso

## ⚙️ Configuración Avanzada

### Branches de Desarrollo

Para trabajo más seguro:

1. Antigravity sube a rama `dev`
2. Workflow se ejecuta en `dev`
3. Después de revisar, merge a `main`

### Personalización del Workflow

Edita `.github/workflows/antigravity-comet-sync.yml` para:

- Agregar más validaciones
- Cambiar notificaciones
- Añadir integraciones (Slack, Discord, etc.)

## 🆘 Troubleshooting

### Problema: El workflow no se ejecuta

**Solución**: Verifica que los archivos estén en las carpetas correctas (`css/`, `js/`, `images/`)

### Problema: Errores de autenticación

**Solución**: Regenera tu Personal Access Token y actualiza Antigravity

### Problema: Conflictos de merge

**Solución**: Siempre haz pull antes de push

## 📚 Recursos Adicionales

- [Documentación de GitHub API](https://docs.github.com/en/rest)
- [GitHub Actions](https://docs.github.com/en/actions)
- [Comet by Perplexity](https://www.perplexity.ai)

## 🎉 ¡Listo para Empezar!

Ahora Antigravity y Comet pueden trabajar juntos de forma automática. Solo tienes que:

1. Desarrollar en local
2. Dejar que Antigravity suba los archivos
3. Revisar los resultados con Comet
4. Repetir el ciclo

---

**Última actualización**: Enero 2026  
**Creado por**: Comet (Perplexity AI)
