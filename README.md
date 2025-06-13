# 🖥️ Radiopatito 42

Un userscript para mejorar la visualización de usuarios en los clústeres de la intranet de 42.

## 📋 Descripción

**Radiopatito 42** es un userscript que mejora la experiencia de visualización en la sección de clústeres de la intranet de 42 (`meta.intra.42.fr/clusters`). Permite ver de forma ampliada las imágenes de perfil de todos los estudiantes conectados en los clústeres, junto con información útil como su login y el ordenador que están utilizando.

## ⚠️ Disclaimer

**Este userscript contiene bromas internas, emojis excesivos y algunas faltas de ortografía intencionales** que forman parte del humor entre mi grupo de amigos de 42. Lo comparto porque funciona bastante bien y puede ser útil para otros estudiantes.

**¿Quieres eliminarlo?** Si prefieres una versión más seria, sin bromas o en otro idioma, ve directamente a la sección **[🌍 Personalización e internacionalización](#-personalización-e-internacionalización)** donde se explica cómo cambiar todos los textos de la interfaz.

**Créditos**: Este userscript empezó un día de aburrimiento con Claude Sonnet 4 de Claude.ai y poco a poco se ha ido puliendo y mejorando.

---

### ✨ Características

- 🔍 **Imágenes ampliadas**: Visualiza las fotos de perfil 15 veces más grandes que el tamaño original
- 👥 **Vista de cuadrícula**: Organiza todas las imágenes en una cuadrícula responsive
- 🏢 **Filtros por clúster**: Filtra usuarios por Clúster A (car*) o Clúster B (cbr*)
- ❤️‍🔥 **Sistema de favoritos**: Añade y gestiona una lista de tus "panas" favoritos
- 💤 **Usuarios offline**: Ve el estado de tus favoritos aunque no estén conectados
- 🔎 **Buscador de usuarios**: Busca patitos específicos por username
- 📊 **Información detallada**: Muestra el login del usuario y el ID del ordenador
- 🔗 **Enlaces directos**: Click en cualquier imagen para ir al perfil del usuario
- 🌍 **Textos configurables**: Sistema de internacionalización fácil de modificar
- 🎨 **Interfaz moderna**: Diseño dark con bordes redondeados y sombras
- 📱 **Responsive**: Se adapta a diferentes tamaños de pantalla
- ⚡ **Gestión de errores**: Manejo elegante de imágenes que no cargan
- 🎲 **Imagen aleatoria**: Si un usuario no existe, muestra una imagen consoladora
- 💾 **Persistencia**: Los favoritos se guardan permanentemente

## 🚀 Instalación

### Paso 1: Instalar un gestor de userscripts

### 🖥️ Compatibilidad PC
- ✅ **Violentmonkey** (Recomendado para escritorio)
- ✅ **Tampermonkey** (Solo firefox en escritorio)
- ❓ **Greasemonkey** (No probado)

### Paso 2: Instalar el script

Tienes dos opciones para instalar **Radiopatito 42**:

#### 🌟 Opción A: Copiar y pegar el código (Recomendado)

1. Instala [Violentmonkey](https://violentmonkey.github.io/) en tu navegador
2. Copia el código completo del userscript desde GitHub:
   - Ve al archivo `Radiopatito_42` en este repositorio
   - Haz click en **"Raw"** para ver el código sin formato
   - Selecciona todo el código (`Ctrl+A`) y cópialo (`Ctrl+C`)
3. Abre el dashboard de Violentmonkey
4. Haz click en **"+ Nuevo"** o **"New Script"**
5. **Borra todo** el contenido que aparece por defecto
6. **Pega el código** del userscript (`Ctrl+V`)
7. Guarda el script (`Ctrl+S`)

#### 📁 Opción B: Arrastrar archivo

1. Instala [Violentmonkey](https://violentmonkey.github.io/) en tu navegador
2. Descarga el archivo `Radiopatito_42` desde este repositorio
3. Arrastra el archivo al dashboard de Violentmonkey o haz click en "Install" cuando se abra automáticamente

### Paso 3: Activar el script

1. **Ve a la página de clústeres**: Navega a `https://meta.intra.42.fr/clusters`
2. **Refresca la página** si ya estabas en esa URL antes de instalar el script
3. **¡Listo!** Deberías ver el botón **"Lo mismo pero grande"** en la esquina inferior derecha

**⚠️ Permisos requeridos**: El script ahora requiere permisos de almacenamiento (`GM_setValue` y `GM_getValue`) para guardar favoritos.

### 📱 Compatibilidad móvil

**Radiopatito 42** es compatible con la versión móvil de Chrome usando **Tampermonkey**.

Compatibilidad adicional:
- ❓ **Greasemonkey** (No probado)
- ❓ **Violentmonkey** (No probado)
<img src="radiopatito_mobile.jpg" alt="Vista móvil de Radiopatito 42" width="200">
*Radiopatito 42 funcionando en Chrome móvil con Tampermonkey*

## 🎯 Uso

1. Navega a la sección de clústeres en la intranet: `https://meta.intra.42.fr/clusters*`
2. Verás un botón en la esquina inferior derecha que dice **"Lo mismo pero grande"**
3. Haz click en el botón para abrir la vista ampliada
4. Disfruta de ver todos los "patitos" 🦆 conectados en una vista mejorada

### 🖱️ Controles principales

- **Botón principal**: Abre/actualiza la vista de imágenes ampliadas
- **Botón × (superior derecho)**: Cierra la vista ampliada
- **Botón 🔍 (superior izquierdo)**: Abre el buscador de usuarios
- **Click en imagen**: Va al perfil del usuario en una nueva pestaña
- **Scroll**: El título se desvanece automáticamente al hacer scroll

### 🏢 Filtros por clúster

Una vez abierta la vista ampliada, encontrarás **cuatro botones** de filtro en la parte superior:

- **Todo 42**: Muestra todos los usuarios conectados (por defecto)
- **Clúster A**: Filtra solo usuarios en estaciones que empiecen por "car" (ej: car1s1)
- **Clúster B**: Filtra solo usuarios en estaciones que empiecen por "cbr" (ej: cbr1s1)
- **❤️‍🔥 Los panas ❤️‍🔥**: **NUEVO** - Muestra tu lista de favoritos

El título se actualiza automáticamente para mostrar cuántos patitos hay en cada clúster.

### ❤️‍🔥 Sistema de favoritos - ¡NUEVA FUNCIONALIDAD!

#### Gestión de favoritos

Al hacer click en "❤️‍🔥 Los panas ❤️‍🔥", accedes a tu lista personal de favoritos con dos botones de gestión:

- **➕ Añadir pana**: Añade nuevos usuarios a tu lista de favoritos
- **💔 Divorcio**: Elimina usuarios de tu lista de favoritos

#### Estados de favoritos

Los usuarios favoritos pueden aparecer en dos estados:

1. **🟢 Online (Conectado)**:
   - Imagen normal del perfil
   - ID del ordenador donde están conectados
   - Enlace directo al perfil

2. **💤 Offline (Desconectado)**:
   - Imagen aleatoria de [Picsum](https://picsum.photos/)
