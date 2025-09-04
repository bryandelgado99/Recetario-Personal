# 🍳 Mi Recetario Personal

Un blog de recetas personal construido con Astro que permite crear recetas fácilmente usando archivos Markdown.

## 🚀 Características

- **Recetas en Markdown**: Escribe recetas usando archivos `.md` simples
- **Técnicas y Consejos**: Sección dedicada a guías culinarias reutilizables
- **Layout automático**: Las recetas y técnicas se renderizan automáticamente con diseño profesional
- **Componentes reutilizables**: Ingredientes, pasos y notas se muestran de forma consistente
- **Enlaces cruzados**: Vincula técnicas desde las recetas y viceversa
- **Responsive**: Funciona perfectamente en móviles y escritorio
- **Índices automáticos**: Las páginas principales se actualizan automáticamente

## 📁 Estructura del Proyecto

```
src/
├── layouts/
│   ├── RecipeLayout.astro          # Layout base para recetas
│   ├── MarkdownRecipeLayout.astro  # Layout específico para recetas MD
│   └── TechniqueLayout.astro       # Layout para técnicas culinarias
├── components/
│   ├── IngredientsList.astro       # Componente para ingredientes
│   ├── RecipeSteps.astro           # Componente para pasos
│   └── RecipeNotes.astro           # Componente para notas y consejos
└── pages/
    ├── index.astro                 # Página principal con navegación
    ├── recetas/
    │   └── pie-de-limon.md         # Ejemplo de receta
    └── tecnicas/
        ├── index.astro             # Índice de técnicas
        ├── activar-levadura.md     # Ejemplo de técnica
        └── punto-nieve.md          # Otro ejemplo
```

## ✨ Cómo Crear Contenido Nuevo

### 🍳 Nueva Receta
1. **Copia el template**: Duplica `template-receta.md` (en la raíz del proyecto)
2. **Muévelo a recetas**: Colócalo en `src/pages/recetas/` con nombre descriptivo
3. **Actualiza el layout**: Cambia la ruta a `../../layouts/MarkdownRecipeLayout.astro`
4. **Añade la imagen**: Coloca tu imagen en `public/images/`
5. **Completa el frontmatter**: Información de la receta
6. **Escribe el contenido**: Información adicional en Markdown

### 📚 Nueva Técnica Culinaria
1. **Copia el template**: Duplica `template-tecnica.md` (en la raíz del proyecto)
2. **Muévelo a técnicas**: Colócalo en `src/pages/tecnicas/` con nombre descriptivo
3. **Actualiza el layout**: Cambia la ruta a `../../layouts/TechniqueLayout.astro`
4. **Añade la imagen**: Coloca tu imagen en `public/images/`
5. **Completa el frontmatter**: Información de la técnica
6. **Escribe la guía**: Pasos detallados y consejos

### 🔗 Enlaces Cruzados
- **En recetas**: Referencia técnicas con `[activar levadura](/tecnicas/activar-levadura)`
- **En técnicas**: Lista recetas relacionadas en el frontmatter `relatedRecipes`

## 🖼️ Manejo de Imágenes

### Añadir Imágenes a tus Recetas

1. **Guarda la imagen**: Coloca tu archivo de imagen en la carpeta `src/assets/`
   - Formatos soportados: `.jpg`, `.jpeg`, `.png`, `.gif`, `.webp`
   - Nombres recomendados: `nombre-receta.jpg`

2. **Referencia en el frontmatter**: Usa solo el nombre del archivo
   ```yaml
   image: "mi-receta.jpg"
   ```

3. **Optimización automática**: Astro optimizará la imagen automáticamente para:
   - Mejor rendimiento de carga
   - Diferentes tamaños de pantalla
   - Formatos modernos cuando sea posible

### Ejemplo de Estructura
```
recetario/
├── template-receta.md            # Template para copiar
├── src/
│   ├── assets/
│   │   ├── pie-limon.jpg
│   │   ├── carbonara.jpg
│   │   └── tortilla-espanola.jpg
│   └── pages/
│       └── recetas/
│           ├── pie-limon.md      # image: "pie-limon.jpg"
│           ├── carbonara.md      # image: "carbonara.jpg"
│           └── tortilla-espanola.md  # image: "tortilla-espanola.jpg"
```

### Ejemplo de Frontmatter

```yaml
---
layout: ../../layouts/MarkdownRecipeLayout.astro
title: "Mi Receta Deliciosa"
description: "Una receta increíble que te encantará"
prepTime: "15 min"
cookTime: "30 min"
servings: 4
difficulty: "Fácil"
tags: ["Vegetariano", "Rápido", "Saludable"]
image: "mi-receta.jpg"  # Archivo en src/assets/
ingredients:
  - "2 tazas de ingrediente principal"
  - "1 cucharada de condimento"
  - "Sal y pimienta al gusto"
steps:
  - "Prepara los ingredientes"
  - "Cocina siguiendo estos pasos"
  - "Sirve y disfruta"
notes:
  - "Consejo útil para mejorar el resultado"
  - "Variación interesante de la receta"
notesType: "tip"
---
```

## 🎨 Personalización

### Tipos de Notas

- `tip`: Consejos útiles (fondo verde)
- `warning`: Advertencias importantes (fondo amarillo)
- `info`: Información adicional (fondo azul)

### Niveles de Dificultad

- `Fácil`: Verde
- `Intermedio`: Naranja
- `Difícil`: Rojo

## 🛠️ Comandos de Desarrollo

```bash
# Instalar dependencias
npm install

# Servidor de desarrollo
npm run dev

# Construir para producción
npm run build

# Vista previa de la build
npm run preview
```

## 📝 Consejos de Uso

1. **Imágenes**: Coloca las imágenes en `src/assets/` y referéncialas solo con el nombre del archivo (ej: `"mi-receta.jpg"`)
2. **URLs**: Las recetas se generan automáticamente en `/recetas/nombre-del-archivo`
3. **Orden**: Las recetas aparecen ordenadas alfabéticamente en la página principal
4. **Markdown**: Puedes usar cualquier elemento de Markdown en el contenido adicional
5. **Formatos de imagen**: Soporta JPG, PNG, GIF y WebP
6. **Optimización**: Astro optimiza automáticamente las imágenes para mejor rendimiento

## 🎯 Próximas Mejoras

- [ ] Búsqueda y filtrado de recetas
- [ ] Categorías de recetas
- [ ] Tiempo de lectura estimado
- [ ] Valoraciones y comentarios
- [ ] Exportar recetas a PDF
- [ ] Modo oscuro

¡Disfruta creando tu colección personal de recetas! 👨‍🍳👩‍🍳
