---
layout: ./src/layouts/MarkdownRecipeLayout.astro
title: "Nombre de tu Receta"
description: "Descripción breve y atractiva de la receta"
prepTime: "15 min"
cookTime: "30 min"
servings: 4
difficulty: "Fácil" # Fácil, Intermedio, Difícil
tags: ["Tag1", "Tag2", "Tag3"]
image: "nombre-imagen.jpg" # Nombre del archivo en src/assets/ (ej: "mi-receta.jpg")
ingredients:
  - "Ingrediente 1 con cantidad"
  - "Ingrediente 2 con cantidad"
  - "Ingrediente 3 con cantidad"
steps:
  - "Primer paso detallado de la preparación"
  - "Segundo paso con instrucciones claras"
  - "Tercer paso y así sucesivamente"
notes:
  - "Consejo útil número 1"
  - "Nota importante número 2"
  - "Truco o variación número 3"
notesType: "tip" # tip, warning, info
---

## Sección Adicional (Opcional)

Aquí puedes añadir cualquier contenido adicional en Markdown:

- Historia del plato
- Variaciones regionales
- Maridajes recomendados
- Información nutricional
- Anécdotas personales

### Subsección

Puedes usar todos los elementos de Markdown:

> Citas importantes o consejos destacados

**Texto en negrita** para enfatizar puntos importantes.

*Texto en cursiva* para notas adicionales.

### Lista de Variaciones

1. Primera variación
2. Segunda variación
3. Tercera variación

---

## 📝 Instrucciones de Uso

1. **Copia este archivo** a `src/pages/recetas/` con un nuevo nombre
2. **Cambia el layout** a `../../layouts/MarkdownRecipeLayout.astro`
3. **Añade tu imagen** a `src/assets/`
4. **Completa todos los campos** del frontmatter
5. **Escribe tu contenido** en Markdown

**Nota**: Este es un archivo template. Cópialo a `src/pages/recetas/` y renómbralo para crear nuevas recetas.