# 🖥️ Radiopatito 42

Un userscript para mejorar la visualización de usuarios en los clusters de la intranet de 42.

## 📋 Descripción

**Radiopatito 42** es un userscript que mejora la experiencia de visualización en la sección de clusters de la intranet de 42 (`meta.intra.42.fr/clusters`). Permite ver de forma ampliada las imágenes de perfil de todos los estudiantes conectados en los clusters, junto con información útil como su login y el ordenador que están utilizando.

### ✨ Características

- 🔍 **Imágenes ampliadas**: Visualiza las fotos de perfil 15 veces más grandes que el tamaño original
- 👥 **Vista de cuadrícula**: Organiza todas las imágenes en una cuadrícula responsive
- 🏢 **Filtros por cluster**: Filtra usuarios por Cluster A (car*) o Cluster B (cbr*)
- 🔎 **Buscador de usuarios**: Busca patitos específicos por username
- 📊 **Información detallada**: Muestra el login del usuario y el ID del ordenador
- 🔗 **Enlaces directos**: Click en cualquier imagen para ir al perfil del usuario
- 🎨 **Interfaz moderna**: Diseño dark con bordes redondeados y sombras
- 📱 **Responsive**: Se adapta a diferentes tamaños de pantalla
- ⚡ **Gestión de errores**: Manejo elegante de imágenes que no cargan
- 🎲 **Imagen aleatoria**: Si un usuario no existe, muestra una imagen consoladora

## 🚀 Instalación

### Paso 1: Instalar un gestor de userscripts

El script ha sido probado y **funciona correctamente** con:
- ✅ **Violentmonkey** (Recomendado para escritorio)
- ✅ **Tampermonkey** (Solo firefox en escritorio)

### 📱 Compatibilidad móvil

**Radiopatito 42** es compatible con la versión móvil de Chrome usando **Tampermonkey**.

Compatibilidad adicional:
- ❓ **Greasemonkey** (No probado)
- ❓ **Violentmonkey** (No probado)

### Paso 2: Instalar el script

1. Instala [Violentmonkey](https://violentmonkey.github.io/) en tu navegador
2. Descarga el archivo `Radiopatito_42` desde este repositorio
3. Arrastra el archivo al dashboard de Violentmonkey o haz click en "Install" cuando se abra automáticamente

## 📸 Radiopatito en móvil!

<img src="radiopatito_mobile.jpg" alt="Vista móvil de Radiopatito 42" width="200">
*Radiopatito 42 funcionando en Chrome móvil con Tampermonkey*

## 🎯 Uso

1. Navega a la sección de clusters en la intranet: `https://meta.intra.42.fr/clusters*`
2. Verás un botón en la esquina inferior derecha que dice **"Lo mismo pero grande"**
3. Haz click en el botón para abrir la vista ampliada
4. Disfruta de ver todos los "patitos" 🦆 conectados en una vista mejorada

### 🖱️ Controles principales

- **Botón principal**: Abre/actualiza la vista de imágenes ampliadas
- **Botón × (superior derecho)**: Cierra la vista ampliada
- **Botón 🔍 (superior izquierdo)**: Abre el buscador de usuarios
- **Click en imagen**: Va al perfil del usuario en una nueva pestaña
- **Scroll**: El título se desvanece automáticamente al hacer scroll

### 🏢 Filtros por cluster

Una vez abierta la vista ampliada, encontrarás tres botones de filtro en la parte superior:

- **Todo 42**: Muestra todos los usuarios conectados (por defecto)
- **Cluster A**: Filtra solo usuarios en estaciones que empiecen por "car" (ej: car1s1)
- **Cluster B**: Filtra solo usuarios en estaciones que empiecen por "cbr" (ej: cbr1s1)

El título se actualiza automáticamente para mostrar cuántos patitos hay en cada cluster.

### 🔎 Buscador de usuarios

El buscador te permite encontrar patitos específicos:

1. **Acceso**: Click en el botón 🔍 en la esquina superior izquierda
2. **Búsqueda**: Escribe el username exacto del usuario
3. **Métodos de búsqueda**:
   - Click en el botón "Buscar"
   - Presiona Enter
4. **Resultados**:
   - **Usuario encontrado**: Muestra "🎉 ¡Patito encontrado! 🎉" con la tarjeta del usuario
   - **Usuario no encontrado**: Muestra "❌ Patito no encontrado ❌" con una imagen aleatoria consoladora de [Picsum](https://picsum.photos/)

#### Características del buscador:
- **Búsqueda case-insensitive**: No importa si escribes en mayúsculas o minúsculas
- **Validación**: Avisa si el campo está vacío
- **Imágenes aleatorias**: Cada búsqueda fallida muestra una imagen diferente
- **Atajos de teclado**: 
  - `Enter` para buscar
  - `Escape` para cerrar
- **Auto-focus**: El campo de búsqueda se selecciona automáticamente

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
- Filtrado dinámico por clusters basado en IDs de estaciones
- Sistema de búsqueda con validación y feedback visual
- Gestión de estados de scroll para UX mejorada
- Manejo de errores de carga de imágenes
- Optimizaciones de rendimiento (lazy loading, document fragments)
- Gestión de memoria y cleanup de event listeners

### Optimizaciones de rendimiento

- **Lazy loading**: Las imágenes se cargan bajo demanda
- **Document fragments**: Operaciones DOM por lotes para mejor rendimiento
- **Throttled scrolling**: Eventos de scroll optimizados
- **Memory cleanup**: Limpieza automática de event listeners y elementos DOM

## 🎨 Interfaz de usuario

El script proporciona:

### Vista principal
- **Contador dinámico**: "Habemos X 👨‍💻 patitos 👩‍💻 [en Cluster A/B]"
- **Grid responsive**: Se adapta automáticamente al tamaño de pantalla
- **Información de usuario**: Login y ID de estación claramente visible

### Controles de navegación
- **Botones de filtro**: Interfaz intuitiva con feedback visual
- **Modal de búsqueda**: Diseño limpio y funcional
- **Botones de acción**: Posicionamiento fijo para fácil acceso

## 🤝 Contribuir

¿Tienes ideas para mejorar Radiopatito 42? ¡Las contribuciones son bienvenidas!

1. Fork este repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Añade nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

### Ideas para futuras mejoras

- [ ] Notificaciones de usuarios favoritos

## 📝 Notas

- El script se ejecuta automáticamente después de 1 segundo de cargar la página
- Las imágenes se redimensionan manteniendo la proporción (`object-fit: contain`)
- Compatible con el sistema de tooltips de la intranet de 42
- Incluye logging en consola para debugging
- El buscador solo busca entre usuarios actualmente conectados en los clusters
- Los filtros por cluster funcionan con el patrón estándar de IDs de 42

## 🔧 Solución de problemas

### El script no funciona
- Verifica que Violentmonkey/Tampermonkey esté instalado y habilitado
- Asegúrate de estar en la URL correcta: `https://meta.intra.42.fr/clusters*`
- Comprueba la consola del navegador para errores

### No aparecen usuarios
- Verifica que haya usuarios conectados en los clusters
- Comprueba que la página haya cargado completamente
- Intenta refrescar la página

### El buscador no encuentra usuarios
- Asegúrate de escribir el username exacto
- Recuerda que solo busca entre usuarios actualmente conectados
- Verifica que el usuario esté realmente en algún cluster

### Problemas en móvil
- Asegúrate de usar Chrome con Tampermonkey instalado
- Verifica que el script esté habilitado en Tampermonkey
- Comprueba que estés accediendo desde la URL correcta de la intranet

## 📄 Licencia

Este proyecto está bajo una licencia abierta. Siéntete libre de usar, modificar y distribuir el código.

## 🏫 Sobre 42

Este script está diseñado específicamente para la red de escuelas 42. Si eres estudiante de 42, ¡esperamos que encuentres útil esta herramienta para visualizar mejor a tus compañeros en los clusters!

---

*Hecho con ❤️ para la comunidad de 42*
