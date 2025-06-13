# 🖥️ Radiopatito 42

Un userscript para mejorar la visualización de usuarios en los clusters de la intranet de 42.

## 📋 Descripción

**Radiopatito 42** es un userscript que mejora la experiencia de visualización en la sección de clusters de la intranet de 42 (`meta.intra.42.fr/clusters`). Permite ver de forma ampliada las imágenes de perfil de todos los estudiantes conectados en los clusters, junto con información útil como su login y el ordenador que están utilizando.

### ✨ Características

- 🔍 **Imágenes ampliadas**: Visualiza las fotos de perfil 15 veces más grandes que el tamaño original
- 👥 **Vista de cuadrícula**: Organiza todas las imágenes en una cuadrícula responsive
- 📊 **Información detallada**: Muestra el login del usuario y el ID del ordenador
- 🔗 **Enlaces directos**: Click en cualquier imagen para ir al perfil del usuario
- 🎨 **Interfaz moderna**: Diseño dark con bordes redondeados y sombras
- 📱 **Responsive**: Se adapta a diferentes tamaños de pantalla
- ⚡ **Gestión de errores**: Manejo elegante de imágenes que no cargan

## 🚀 Instalación

### Paso 1: Instalar un gestor de userscripts

El script ha sido probado y **funciona correctamente** con:
- ✅ **Violentmonkey** (Recomendado)

Compatibilidad conocida:
- ⚠️ **Tampermonkey** (Solo firefox)
- ❓ **Greasemonkey** (No probado)

### Paso 2: Instalar el script

1. Instala [Violentmonkey](https://violentmonkey.github.io/) en tu navegador
2. Descarga el archivo `Radiopatito_42` desde este repositorio
3. Arrastra el archivo al dashboard de Violentmonkey o haz click en "Install" cuando se abra automáticamente

## 🎯 Uso

1. Navega a la sección de clusters en la intranet: `https://meta.intra.42.fr/clusters*`
2. Verás un botón en la esquina inferior derecha que dice **"Lo mismo pero grande"**
3. Haz click en el botón para abrir la vista ampliada
4. Disfruta de ver todos los "patitos" 🦆 conectados en una vista mejorada

### 🖱️ Controles

- **Botón principal**: Abre/actualiza la vista de imágenes ampliadas
- **Botón ×**: Cierra la vista ampliada (esquina superior derecha)
- **Click en imagen**: Va al perfil del usuario en una nueva pestaña
- **Scroll**: El título se desvanece automáticamente al hacer scroll

## 🛠️ Detalles técnicos

### Características del código

- **Namespace**: `Violentmonkey Scripts`
- **Versión**: 42 (porque... 42! 🎯)
- **Permisos**: Ninguno requerido (`@grant none`)
- **Dominio**: Solo funciona en `https://meta.intra.42.fr/clusters*`

### Funcionalidades implementadas

- Detección automática de imágenes SVG con atributos `xlink:href` o `href`
- Extracción de metadatos de tooltips y atributos de elementos
- Amplificación inteligente de imágenes (15x el tamaño original)
- Grid CSS responsive con `minmax(300px, 1fr)`
- Gestión de estados de scroll para UX mejorada
- Manejo de errores de carga de imágenes

## 🎨 Capturas de pantalla

El script muestra:
- Contador total de usuarios: "Habemos X 👨‍💻 patitos 👩‍💻"
- Grid de imágenes ampliadas con información del usuario
- Navegación intuitiva con botones de control

## 🤝 Contribuir

¿Tienes ideas para mejorar Radiopatito 42? ¡Las contribuciones son bienvenidas!

1. Fork este repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Añade nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

## 📝 Notas

- El script se ejecuta automáticamente después de 1 segundo de cargar la página
- Las imágenes se redimensionan manteniendo la proporción (`object-fit: contain`)
- Compatible con el sistema de tooltips de la intranet de 42
- Incluye logging en consola para debugging

## 📄 Licencia

Este proyecto está bajo una licencia abierta. Siéntete libre de usar, modificar y distribuir el código.

## 🏫 Sobre 42

Este script está diseñado específicamente para la red de escuelas 42. Si eres estudiante de 42, ¡esperamos que encuentres útil esta herramienta para visualizar mejor a tus compañeros en los clusters!

---

*Hecho con ❤️ para la comunidad de 42*
