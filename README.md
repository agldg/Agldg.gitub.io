# MarkItDown Web — GitHub Pages

Interfaz web para convertir archivos a Markdown, funciona **100% en el navegador** sin servidor.

## 🚀 Deploy en GitHub Pages (3 pasos)

1. **Crea un repositorio** en GitHub (puede ser público o privado con plan Pro)

2. **Sube el archivo** `index.html` a la raíz del repositorio

3. **Activa GitHub Pages:**
   - Ve a **Settings → Pages**
   - En *Source* selecciona rama `main`, carpeta `/ (root)`
   - Haz clic en **Save**
   - En ~1 minuto tendrás tu link: `https://tu-usuario.github.io/tu-repo/`

## 🔑 API key de Anthropic

La herramienta usa la API de Claude para procesar los archivos.

- Obtén tu key gratis en [console.anthropic.com](https://console.anthropic.com)
- Se guarda **solo en tu navegador** (localStorage), nunca se envía a ningún servidor externo
- Cada usuario ingresa su propia key

## 📁 Formatos soportados

| Formato | Método |
|---|---|
| PDF | Claude API (visión de documentos) |
| Imágenes (PNG, JPG…) | Claude API (visión) |
| HTML | Conversión local |
| CSV | Conversión local a tabla Markdown |
| TXT, MD, JSON, XML… | Lectura directa |
| DOCX, XLSX, PPTX | Claude API (mejor convertir a PDF primero) |

## ⚠️ Limitaciones vs versión con servidor

| Característica | GitHub Pages | Con servidor (server.py) |
|---|---|---|
| Sin instalación | ✅ | ❌ |
| PDF | ✅ | ✅ |
| Imágenes | ✅ | ✅ |
| DOCX / XLSX / PPTX | Parcial | ✅ Completo |
| Sin API key | ❌ | ✅ |
| Archivos >10MB | ❌ | ✅ |

## 💡 Tip

Para archivos Office (.docx, .xlsx, .pptx), la mejor estrategia es exportarlos como PDF desde Word/Excel/PowerPoint antes de subirlos.
